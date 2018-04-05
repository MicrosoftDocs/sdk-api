---
UID: NF:azroles.IAzAuthorizationStore.DeletePropertyItem
title: IAzAuthorizationStore::DeletePropertyItem method
author: windows-driver-content
description: Removes the specified principal from the specified list of principals.
old-location: security\azauthorizationstore_deletepropertyitem.htm
old-project: SecAuthZ
ms.assetid: 7c204a3c-2c5b-44d3-bbab-2765e66da925
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: AZ_PROP_DELEGATED_POLICY_USERS, AZ_PROP_DELEGATED_POLICY_USERS_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AzAuthorizationStore object [Security], DeletePropertyItem method, DeletePropertyItem method [Security], DeletePropertyItem method [Security], AzAuthorizationStore object, DeletePropertyItem method [Security], IAzAuthorizationStore interface, DeletePropertyItem,IAzAuthorizationStore.DeletePropertyItem, IAzAuthorizationStore, IAzAuthorizationStore interface [Security], DeletePropertyItem method, IAzAuthorizationStore::DeletePropertyItem, azroles/IAzAuthorizationStore::DeletePropertyItem, security.azauthorizationstore_deletepropertyitem
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Azroles.dll
api_name:
-	AzAuthorizationStore.DeletePropertyItem
-	IAzAuthorizationStore.DeletePropertyItem
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::DeletePropertyItem method


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
Can also be removed using the <a href="https://msdn.microsoft.com/c27ca754-7808-4c96-8966-0be3960f2926">DeletePolicyAdministrator</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/28be14c8-9e39-4410-a08c-b52bb63d0ce4">DeletePolicyAdministratorName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/948732bb-4d29-402b-bb12-02d2b73bc443">DeletePolicyReader</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/b3375c24-82c3-43fd-a063-8c8079324641">DeletePolicyReaderName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS"></a><a id="az_prop_delegated_policy_users"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/cb00abca-7116-4a71-aed0-87ed9caff0fb">DeleteDelegatedPolicyUser</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS_NAME"></a><a id="az_prop_delegated_policy_users_name"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/a2e7523a-41d3-4fb5-b455-588e0618f51f">DeleteDelegatedPolicyUserName</a> method

</td>
</tr>
</table>
 


### -param varProp [in]

The principal to remove from the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS_NAME, or AZ_PROP_DELEGATED_POLICY_USERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name must be in user principal name (UPN) format (for example, "someone@example.com").


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/bf2962af-0e8f-4c4c-a63a-dfd623308e4d">Submit</a> method to persist any changes made by this method.



