---
title: Overriding the Default Limit for a Namespace
---

<head>
  <link rel="canonical" href="https://ranchermanager.docs.rancher.com/how-to-guides/advanced-user-guides/manage-projects/manage-project-resource-quotas/override-default-limit-in-namespaces"/>
</head>

Although the **Namespace Default Limit** propagates from the project to each namespace when created, in some cases, you may need to increase (or decrease) the quotas for a specific namespace. In this situation, you can override the default limits by editing the namespace.

In the diagram below, the Rancher administrator has a resource quota in effect for their project. However, the administrator wants to override the namespace limits for `Namespace 3` so that it has more resources available. Therefore, the administrator [raises the namespace limits](../../manage-clusters/projects-and-namespaces.md) for `Namespace 3` so that the namespace can access more resources.

<sup>Namespace Default Limit Override</sup>

![Namespace Default Limit Override](/img/rancher-resource-quota-override.svg)

How to: [Editing Namespace Resource Quotas](../../manage-clusters/projects-and-namespaces.md)

### Editing Namespace Resource Quotas

If there is a [resource quota](../../../../pages-for-subheaders/manage-project-resource-quotas.md) configured for a project, you can override the namespace default limit to provide a specific namespace with access to more (or less) project resources.

1. From the **Global** view, open the cluster that contains the namespace for which you want to edit the resource quota.

1. From the main menu, select **Projects/Namespaces**.

1. Find the namespace for which you want to edit the resource quota. Select **&#8942; > Edit**.

1. Edit the Resource Quota **Limits**.  These limits determine the resources available to the namespace. The limits must be set within the configured project limits.

    For more information about each **Resource Type**, see [Resource Quotas](../../../../pages-for-subheaders/manage-project-resource-quotas.md).

    >**Note:**
    >
    >- If a resource quota is not configured for the project, these options will not be available.
    >- If you enter limits that exceed the configured project limits, Rancher will not let you save your edits.

**Result:** Your override is applied to the namespace's resource quota.
