---
UID: NF:azroles.IAzAuthorizationStore.AddPropertyItem
title: IAzAuthorizationStore::AddPropertyItem (azroles.h)
description: Adds the specified principal to the specified list of principals. (IAzAuthorizationStore.AddPropertyItem)
helpviewer_keywords: ["AZ_PROP_DELEGATED_POLICY_USERS","AZ_PROP_DELEGATED_POLICY_USERS_NAME","AZ_PROP_POLICY_ADMINS","AZ_PROP_POLICY_ADMINS_NAME","AZ_PROP_POLICY_READERS","AZ_PROP_POLICY_READERS_NAME","AddPropertyItem","AddPropertyItem method [Security]","AddPropertyItem method [Security]","AzAuthorizationStore object","AddPropertyItem method [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","AddPropertyItem method","IAzAuthorizationStore interface [Security]","AddPropertyItem method","IAzAuthorizationStore.AddPropertyItem","IAzAuthorizationStore::AddPropertyItem","azroles/IAzAuthorizationStore::AddPropertyItem","security.azauthorizationstore_addpropertyitem"]
old-location: security\azauthorizationstore_addpropertyitem.htm
tech.root: security
ms.assetid: 88ac498c-2871-4260-8011-0aea9e6c346d
ms.date: 12/05/2018
ms.keywords: AZ_PROP_DELEGATED_POLICY_USERS, AZ_PROP_DELEGATED_POLICY_USERS_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzAuthorizationStore object, AddPropertyItem method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPropertyItem method, IAzAuthorizationStore interface [Security],AddPropertyItem method, IAzAuthorizationStore.AddPropertyItem, IAzAuthorizationStore::AddPropertyItem, azroles/IAzAuthorizationStore::AddPropertyItem, security.azauthorizationstore_addpropertyitem
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
 - IAzAuthorizationStore::AddPropertyItem
 - azroles/IAzAuthorizationStore::AddPropertyItem
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
 - AzAuthorizationStore.AddPropertyItem
 - IAzAuthorizationStore.AddPropertyItem
---

# IAzAuthorizationStore::AddPropertyItem


## -description

The <b>AddPropertyItem</b> method adds the specified principal to the specified list of principals.

## -parameters

### -param lPropId [in]

Property ID of the  list of principals to which to add the principal specified by the <i>varProp</i> parameter. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS"></a><a id="az_prop_policy_admins"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyadministrator">AddPolicyAdministrator</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyadministratorname">AddPolicyAdministratorName</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyreader">AddPolicyReader</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-addpolicyreadername">AddPolicyReaderName</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS"></a><a id="az_prop_delegated_policy_users"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser">AddDelegatedPolicyUser</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS_NAME"></a><a id="az_prop_delegated_policy_users_name"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyusername">AddDelegatedPolicyUserName</a> method.

</td>
</tr>
</table>

### -param varProp [in]

Principal to add to the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS_NAME, or AZ_PROP_DELEGATED_POLICY_USERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to add to the list. The account name must be in <a href="/windows/desktop/SecGloss/u-gly">user principal name</a> (UPN) format (for example, "someone@example.com").

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-submit">Submit</a> method to persist any changes made by this method.
