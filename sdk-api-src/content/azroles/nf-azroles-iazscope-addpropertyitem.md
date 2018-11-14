---
UID: NF:azroles.IAzScope.AddPropertyItem
title: IAzScope::AddPropertyItem
author: windows-sdk-content
description: Adds the specified principal to the specified list of principals.
old-location: security\iazscope_addpropertyitem.htm
tech.root: secauthz
ms.assetid: 5170079b-9ea6-417c-87f2-bb8835225911
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: AZ_PROP_POLICY_ADMINS, AZ_PROP_POLICY_ADMINS_NAME, AZ_PROP_POLICY_READERS, AZ_PROP_POLICY_READERS_NAME, AddPropertyItem, AddPropertyItem method [Security], AddPropertyItem method [Security],AzScope object, AddPropertyItem method [Security],IAzScope interface, AzScope object [Security],AddPropertyItem method, IAzScope interface [Security],AddPropertyItem method, IAzScope.AddPropertyItem, IAzScope::AddPropertyItem, azroles/IAzScope::AddPropertyItem, security.iazscope_addpropertyitem
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
 - IAzScope.AddPropertyItem
 - AzScope.AddPropertyItem
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
- IAzScope.AddPropertyItem
: 
---

# IAzScope::AddPropertyItem


## -description


The <b>AddPropertyItem</b> method adds the specified principal to the specified list of principals.


## -parameters




### -param lPropId [in]

Property ID of the  list of principals to which to add the principal specified by the <i>varProp</i> parameter. The following table shows the possible values.

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
Can also be added using the <a href="https://msdn.microsoft.com/7aa77615-1f12-4641-877e-87b26343db4d">AddPolicyAdministrator</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_ADMINS_NAME"></a><a id="az_prop_policy_admins_name"></a><dl>
<dt><b>AZ_PROP_POLICY_ADMINS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/a160e4cb-e779-413e-9d8a-5fb9684a48f2">AddPolicyAdministratorName</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS"></a><a id="az_prop_policy_readers"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/dd4d3254-8bcf-46b5-8e7b-d3f076988a7c">AddPolicyReader</a> method

</td>
</tr>
<tr>
<td width="40%"><a id="AZ_PROP_POLICY_READERS_NAME"></a><a id="az_prop_policy_readers_name"></a><dl>
<dt><b>AZ_PROP_POLICY_READERS_NAME</b></dt>
</dl>
</td>
<td width="60%">
Can also be added using the <a href="https://msdn.microsoft.com/6beb02cb-7977-4f3f-b806-420c81f6f0b5">AddPolicyReaderName</a> method

</td>
</tr>
</table>
 


### -param varProp [in]

Principal to add to the list of principals specified by the <i>lPropId</i> parameter.

The variant must be a <b>BSTR</b> variant.

If AZ_PROP_POLICY_ADMINS or AZ_PROP_POLICY_READERS is specified for the <i>lPropId</i> parameter, the string is the text form of the <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">security identifier</a> (SID) of the Windows account to add to the list. If AZ_PROP_POLICY_ADMINS_NAME or AZ_PROP_POLICY_READERS_NAME is specified for the <i>lPropId</i> parameter, the string is the account name of the account to add to the list. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format.


### -param varReserved [in, optional]

Reserved for future use.


## -returns



The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.




## -remarks



You must call the <a href="https://msdn.microsoft.com/en-us/library/Aa378364(v=VS.85).aspx">Submit</a> method to persist any changes made by this method.



