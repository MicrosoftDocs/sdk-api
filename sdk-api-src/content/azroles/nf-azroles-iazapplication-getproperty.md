---
UID: NF:azroles.IAzApplication.GetProperty
title: IAzApplication::GetProperty (azroles.h)
description: Returns the IAzApplication object property with the specified property ID.
helpviewer_keywords: ["AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID","AZ_PROP_APPLICATION_DATA","AZ_PROP_APPLICATION_VERSION","AZ_PROP_APPLY_STORE_SACL","AZ_PROP_CHILD_CREATE","AZ_PROP_DELEGATED_POLICY_USERS","AZ_PROP_DELEGATED_POLICY_USERS_NAME","AZ_PROP_DESCRIPTION","AZ_PROP_GENERATE_AUDITS","AZ_PROP_NAME","AZ_PROP_POLICY_ADMINS","AZ_PROP_POLICY_ADMINS_NAME","AZ_PROP_POLICY_READERS","AZ_PROP_POLICY_READERS_NAME","AZ_PROP_WRITABLE","AzApplication object [Security]","GetProperty method","GetProperty","GetProperty method [Security]","GetProperty method [Security]","AzApplication object","GetProperty method [Security]","IAzApplication interface","IAzApplication interface [Security]","GetProperty method","IAzApplication.GetProperty","IAzApplication::GetProperty","azroles/IAzApplication::GetProperty","security.iazapplication_getproperty"]
old-location: security\iazapplication_getproperty.htm
tech.root: security
ms.assetid: cc2c7a59-497f-403f-8ed1-8a2d5b33c07d
ms.date: 12/05/2018
ms.keywords: AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID, AZ_PROP_APPLICATION_DATA, AZ_PROP_APPLICATION_VERSION, AZ_PROP_APPLY_STORE_SACL, AZ_PROP_CHILD_CREATE, AZ_PROP_DELEGATED_POLICY_USERS, AZ_PROP_DELEGATED_POLICY_USERS_NAME, AZ_PROP_DESCRIPTION, AZ_PROP_GENERATE_AUDITS, AZ_PROP_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AZ_PROP_WRITABLE, AzApplication object [Security],GetProperty method, GetProperty, GetProperty method [Security], GetProperty method [Security],AzApplication object, GetProperty method [Security],IAzApplication interface, IAzApplication interface [Security],GetProperty method, IAzApplication.GetProperty, IAzApplication::GetProperty, azroles/IAzApplication::GetProperty, security.iazapplication_getproperty
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication::GetProperty
 - azroles/IAzApplication::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.GetProperty
 - AzApplication.GetProperty
---

# IAzApplication::GetProperty


## -description

The <b>GetProperty</b> method returns the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object property  with the specified property ID.

## -parameters

### -param lPropId [in]

Property ID of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object property  to return. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID"></a><a id="az_prop_application_authz_interface_clsid"></a><dl>
<dt><b>AZ_PROP_APPLICATION_AUTHZ_INTERFACE_CLSID</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_authzinterfaceclsid">AuthzInterfaceClsid</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_DATA"></a><a id="az_prop_application_data"></a><dl>
<dt><b>AZ_PROP_APPLICATION_DATA</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applicationdata">ApplicationData</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLICATION_VERSION"></a><a id="az_prop_application_version"></a><dl>
<dt><b>AZ_PROP_APPLICATION_VERSION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_version">Version</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_APPLY_STORE_SACL"></a><a id="az_prop_apply_store_sacl"></a><dl>
<dt><b>AZ_PROP_APPLY_STORE_SACL</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_applystoresacl">ApplyStoreSacl</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_CHILD_CREATE"></a><a id="az_prop_child_create"></a><dl>
<dt><b>AZ_PROP_CHILD_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Determines whether the current user has permission to create child objects. This value is <b>TRUE</b> if the current user has permission; otherwise, <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS"></a><a id="az_prop_delegated_policy_users"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusers">DelegatedPolicyUsers</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS_NAME"></a><a id="az_prop_delegated_policy_users_name"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusersname">DelegatedPolicyUsersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DESCRIPTION"></a><a id="az_prop_description"></a><dl>
<dt><b>AZ_PROP_DESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_description">Description</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_GENERATE_AUDITS"></a><a id="az_prop_generate_audits"></a><dl>
<dt><b>AZ_PROP_GENERATE_AUDITS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_generateaudits">GenerateAudits</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_NAME"></a><a id="az_prop_name"></a><dl>
<dt><b>AZ_PROP_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_name">Name</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS"></a><a id="az_prop_policy_admins"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyadministrators">PolicyAdministrators</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyadministratorsname">PolicyAdministratorsName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyreaders">PolicyReaders</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyreadersname">PolicyReadersName</a> property

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_WRITABLE"></a><a id="az_prop_writable"></a><dl>
<dt><b>AZ_PROP_WRITABLE</b></dt>
</dl>
</td>
<td width="60%">
Also accessed through the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_writable">Writable</a> property

</td>
</tr>
</table>

### -param varReserved [in, optional]

Reserved for future use.

### -param pvarProp [out]

A pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object property.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.