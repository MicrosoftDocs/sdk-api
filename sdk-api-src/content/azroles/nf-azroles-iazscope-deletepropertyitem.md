---
UID: NF:azroles.IAzScope.DeletePropertyItem
title: IAzScope::DeletePropertyItem
author: windows-sdk-content
description: Removes the specified principal from the specified list of principals.
old-location: security\iazscope_deletepropertyitem.htm
tech.root: SecAuthZ
ms.assetid: 16500d05-c5bf-4d09-8649-ebf58407120d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AzScope object [Security],DeletePropertyItem method, DeletePropertyItem, DeletePropertyItem method [Security], DeletePropertyItem method [Security],AzScope object, DeletePropertyItem method [Security],IAzScope interface, IAzScope interface [Security],DeletePropertyItem method, IAzScope.DeletePropertyItem, IAzScope::DeletePropertyItem, azroles/IAzScope::DeletePropertyItem, security.iazscope_deletepropertyitem
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
 - IAzScope.DeletePropertyItem
 - AzScope.DeletePropertyItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzScope.DeletePropertyItem
: 
---

# IAzScope::DeletePropertyItem


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
Can also be removed using the <a href="https://msdn.microsoft.com/23077da5-5475-45c6-87c0-b38f6c05d386">DeletePolicyAdministrator</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/6314e1d5-e5ea-42c4-9457-dad5d6f57897">DeletePolicyAdministratorName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/c328a838-ae81-463d-8aa5-827071f58747">DeletePolicyReader</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be removed using the <a href="https://msdn.microsoft.com/e65af2a2-c7f7-483c-af05-342075218158">DeletePolicyReaderName</a> method

</td>
</tr>
</table>
 


### -param varProp [in]

Principal to remove from the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS or AZ_PROP_POLICY_READERS is specified for the <i>lPropId</i> parameter, the string is the text form of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the Windows account to remove from the list. If AZ_PROP_POLICY_ADMINS_NAME or AZ_PROP_POLICY_READERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to remove from the list. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.



