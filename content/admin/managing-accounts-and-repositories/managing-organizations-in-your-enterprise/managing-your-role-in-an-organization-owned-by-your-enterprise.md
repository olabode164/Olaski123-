---
title: Managing your role in an organization owned by your enterprise
intro: You can manage your membership in any organization owned by your enterprise and change your role within the organization.
permissions: Enterprise owners can manage their role in an organization owned by the enterprise.
redirect_from:
  - /admin/user-management/managing-organizations-in-your-enterprise/managing-your-role-in-an-organization-owned-by-your-enterprise
versions:
  feature: enterprise-owner-join-org
type: how_to
topics:
  - Administrator
  - Enterprise
  - Organizations
shortTitle: Manage your organization roles
---

## About role management

You can choose to join an organization owned by your enterprise as a member or as an organization owner, change your role within the organization, or leave the organization.

{% ifversion ghec %}

> [!WARNING]
> If an organization uses SCIM to provision users, joining the organization this way could have unintended consequences. For more information, see "[AUTOTITLE](/organizations/managing-saml-single-sign-on-for-your-organization/about-scim-for-organizations)."

{% endif %}

For information about managing other people's roles in an organization, see "[AUTOTITLE](/organizations/managing-membership-in-your-organization)" and "[AUTOTITLE](/organizations/managing-peoples-access-to-your-organization-with-roles)."

## Managing your role with the enterprise settings

You can join an organization owned by your enterprise and manage your role within the organization, directly from the settings for your enterprise account.

{% ifversion ghec %}

If an organization enforces SAML single sign-on (SSO), you cannot use the enterprise settings to join the organization. Instead, you must join the organization using that organization's identity provider (IdP). Then, you can manage your role in your enterprise settings. For more information, see "[Joining an organization that enforces SAML SSO](#joining-an-organization-that-enforces-saml-sso)."

{% endif %}

{% data reusables.enterprise-accounts.access-enterprise %}
1. Next to the organization you want to manage your role in, select the {% octicon "gear" aria-label="Organization settings" %} dropdown menu and click **Join as an organization owner** or **Join as an organization member**.

   {% data reusables.enterprise-accounts.organization-settings-dropdown %}

{% ifversion ghec %}

## Joining an organization that enforces SAML SSO

If an organization enforces SAML SSO, you cannot use the enterprise settings to join the organization. Instead, you must join the organization using that organization's identity provider (IdP).

1. You must be assigned access in your IdP to the application for {% data variables.product.prodname_ghe_cloud %} that is used by the organization. If you're unable to configure your IdP yourself, contact your IdP administrator.
1. Authenticate to the organization using SAML SSO.

   * If the organization uses SCIM, accept the organization invitation that will be generated by the SCIM integration.
   * If the organization does not use SCIM, visit the following URL, replacing ORGANIZATION with the name of the organization, then follow the prompts to authenticate.

     `https://github.com/orgs/ORGANIZATION/sso`

After you've joined the organization, you can use the enterprise settings to manage your role in the organization, such as becoming an organization owner. For more information, see "[Managing your role with the enterprise settings](#managing-your-role-with-the-enterprise-settings)."

{% endif %}
