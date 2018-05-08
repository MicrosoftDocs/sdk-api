---
UID: NF:azroles.IAzApplication.DeletePropertyItem
title: IAzApplication::DeletePropertyItem
author: windows-driver-content
description: Removes the specified principal from the specified list of principals.
old-location: security\iazapplication_deletepropertyitem.htm
old-project: SecAuthZ
ms.assetid: d7303b03-3b32-407c-a50f-8803b2871a66
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AZ_PROP_DELEGATED_POLICY_USERS, AZ_PROP_DELEGATED_POLICY_USERS_NAME, AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AzApplication object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzApplication object, DeletePropertyItem method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePropertyItem method, IAzApplication.DeletePropertyItem, IAzApplication::DeletePropertyItem, azroles/IAzApplication::DeletePropertyItem, security.iazapplication_deletepropertyitem
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
-	IAzApplication.DeletePropertyItem
-	AzApplication.DeletePropertyItem
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
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
Can also be removed using the <a href="https://msdn.microsoft.com/240dbfbc-ae0f-4a8e-9cbc-b58efb258ad5">DeletePolicyAdministrator</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/6da92103-6de0-4310-b52c-c1441e775da8">DeletePolicyAdministratorName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/aec8b5c4-3c5e-4b91-a10f-40ef05beca1f">DeletePolicyReader</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/1948fb2d-a1ca-4f66-889d-d00f8f265ba5">DeletePolicyReaderName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS"></a><a id="az_prop_delegated_policy_users"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/92e7f4fa-ff86-4ef5-8b87-086dd73966d1">DeleteDelegatedPolicyUser</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_DELEGATED_POLICY_USERS_NAME"></a><a id="az_prop_delegated_policy_users_name"></a><dl>
<dt><b>AZ_PROP_DELEGATED_POLICY_USERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/b6abe8d6-9212-4c92-ba35-d6eaa8df1115">DeleteDelegatedPolicyUserName</a> method

</td>
</tr>
</table>
 


### -param varProp [in]

Principal to remove from the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_READERS, or AZ_PROP_DELEGATED_POLICY_USERS is specified for the <i>lPropId</i> parameter, the string is the text form  of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the  Windows account to remove from the list. If AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS_NAME, or AZ_PROP_DELEGATED_POLICY_USERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name can be in either user principal name (UPN) format (for example,  "someone@example.com") or in the format  of "ExampleDomain\UserName".


### -param varReserved [in, optional]

Reserved for future use.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



