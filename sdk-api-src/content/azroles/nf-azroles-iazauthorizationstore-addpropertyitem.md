---
UID: NF:azroles.IAzAuthorizationStore.AddPropertyItem
title: IAzAuthorizationStore::AddPropertyItem
author: windows-sdk-content
description: Adds the specified principal to the specified list of principals.
old-location: security\azauthorizationstore_addpropertyitem.htm
tech.root: SecAuthZ
ms.assetid: 88ac498c-2871-4260-8011-0aea9e6c346d
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AZ_PROP_DELEGATED_POLICY_USERS, AZ_PROP_DELEGATED_POLICY_USERS_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzAuthorizationStore object, AddPropertyItem method [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],AddPropertyItem method, IAzAuthorizationStore interface [Security],AddPropertyItem method, IAzAuthorizationStore.AddPropertyItem, IAzAuthorizationStore::AddPropertyItem, azroles/IAzAuthorizationStore::AddPropertyItem, security.azauthorizationstore_addpropertyitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
Can also be added by using the <a href="https://msdn.microsoft.com/8d73bc05-1366-4b47-9eaf-4a247ebf8d93">AddPolicyAdministrator</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="https://msdn.microsoft.com/b77348c7-4389-47ba-9f4f-e5643cf992aa">AddPolicyAdministratorName</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="https://msdn.microsoft.com/52872839-1066-4a43-8549-b7f37a0ebe40">AddPolicyReader</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="https://msdn.microsoft.com/3b111542-61d6-4e5d-abf8-0af61161c885">AddPolicyReaderName</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS"></a><a id="az_prop_delegated_policy_users"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="https://msdn.microsoft.com/0c6714e9-489e-4266-a8b5-35c66b0a14f4">AddDelegatedPolicyUser</a> method.

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS_NAME"></a><a id="az_prop_delegated_policy_users_name"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added by using the <a href="https://msdn.microsoft.com/9eeb4670-a3be-46dd-83b4-4ab12a311fe3">AddDelegatedPolicyUserName</a> method.

</td>
</tr>
</table>
 


### -param varProp [in]

Principal to add to the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS_NAME, or AZ_PROP_DELEGATED_POLICY_USERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to add to the list. The account name must be in <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user principal name</a> (UPN) format (for example, "someone@example.com").


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



