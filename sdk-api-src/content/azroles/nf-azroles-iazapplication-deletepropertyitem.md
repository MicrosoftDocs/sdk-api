---
UID: NF:azroles.IAzApplication.DeletePropertyItem
title: IAzApplication::DeletePropertyItem (azroles.h)
description: Removes the specified principal from the specified list of principals. (IAzApplication.DeletePropertyItem)
helpviewer_keywords: ["AZ_PROP_DELEGATED_POLICY_USERS","AZ_PROP_DELEGATED_POLICY_USERS_NAME","AZ_PROP_POLICY_ADMINS","AZ_PROP_POLICY_ADMINS_NAME","AZ_PROP_POLICY_READERS","AZ_PROP_POLICY_READERS_NAME","AzApplication object [Security]","DeletePropertyItem method","DeletePropertyItem","DeletePropertyItem method [Security]","DeletePropertyItem method [Security]","AzApplication object","DeletePropertyItem method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeletePropertyItem method","IAzApplication.DeletePropertyItem","IAzApplication::DeletePropertyItem","azroles/IAzApplication::DeletePropertyItem","security.iazapplication_deletepropertyitem"]
old-location: security\iazapplication_deletepropertyitem.htm
tech.root: security
ms.assetid: d7303b03-3b32-407c-a50f-8803b2871a66
ms.date: 12/05/2018
ms.keywords: AZ_PROP_DELEGATED_POLICY_USERS, AZ_PROP_DELEGATED_POLICY_USERS_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AzApplication object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzApplication object, DeletePropertyItem method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePropertyItem method, IAzApplication.DeletePropertyItem, IAzApplication::DeletePropertyItem, azroles/IAzApplication::DeletePropertyItem, security.iazapplication_deletepropertyitem
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
 - IAzApplication::DeletePropertyItem
 - azroles/IAzApplication::DeletePropertyItem
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
 - IAzApplication.DeletePropertyItem
 - AzApplication.DeletePropertyItem
---

# IAzApplication::DeletePropertyItem


## -description

The <b>DeletePropertyItem</b> method removes the specified principal from the specified  list of principals.

## -parameters

### -param lPropId [in]

Property ID of the  list of principals from which to remove the principal specified by the <i>varProp</i> parameter. The following table shows the possible values.

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
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyadministrator">DeletePolicyAdministrator</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyadministratorname">DeletePolicyAdministratorName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyreader">DeletePolicyReader</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-deletepolicyreadername">DeletePolicyReaderName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS"></a><a id="az_prop_delegated_policy_users"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-deletedelegatedpolicyuser">DeleteDelegatedPolicyUser</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS_NAME"></a><a id="az_prop_delegated_policy_users_name"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-deletedelegatedpolicyusername">DeleteDelegatedPolicyUserName</a> method

</td>
</tr>
</table>

### -param varProp [in]

Principal to remove from the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_READERS, or AZ_PROP_DELEGATED_POLICY_USERS is specified for the <i>lPropId</i> parameter, the string is the text form  of the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) of the  Windows account to remove from the list. If AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS_NAME, or AZ_PROP_DELEGATED_POLICY_USERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name can be in either user principal name (UPN) format (for example,  "someone@example.com") or in the format  of "ExampleDomain\UserName".

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a> method to persist any changes made by this method.
