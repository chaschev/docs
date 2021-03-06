# Access management

Yandex.Cloud users can only perform operations on resources that are permitted under the roles assigned to them. If the user has no roles assigned, all operations are forbidden.

To allow access to resources in {{ message-queue-full-name }}, assign the required roles to the user from the list below. For now, a role can only be assigned for a parent resource (folder or cloud), and roles are inherited by nested resources.

{% note info %}

For more information about role inheritance, see the section [Inheritance of access rights](../../resource-manager/concepts/resources-hierarchy.md#access-rights-inheritance) in the {{ resmgr-name }} documentation.

{% endnote %}

## Assigning roles

To manage message queues, the user must have the appropriate permissions in the cloud and folders where operations will be performed.

To grant the user permissions:

{% include [grant-role-console](../../_includes/grant-role-console.md) %}

## Roles

The list below shows all roles that are considered when verifying access rights in the {{ service-name }} service.

### Service roles

Service roles are roles that allow access to the resources of a particular service. When {{ service-name }} resource access rights are checked, the {{ resmgr-name }} service roles are taken into account.

{% include [cloud-roles](../../_includes/cloud-roles.md) %}

### Primitive roles

You can assign primitive roles to any resource in any service.

#### {{ roles-viewer }}

Users with the `{{ roles-viewer }}` role can view lists of cloud message queues and messages.

#### {{ roles-editor }}

Users with the `{{ roles-editor }}` role can perform any operations on message queues and messages.

The `{{ roles-editor }}` role also includes all `{{ roles-viewer }}` role permissions.

#### {{ roles-admin }}

Users with the `{{ roles-admin }}` role can manage resource access rights, such as allowing other users to create message queues and messages or view their details.

The `{{ roles-admin }}` role also includes all `{{ roles-editor }}` role permissions.

## See also

[Hierarchy of Yandex.Cloud resources](../../resource-manager/concepts/resources-hierarchy.md)

