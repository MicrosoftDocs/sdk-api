---
UID: NF:aclui.IEffectivePermission.GetEffectivePermission
title: IEffectivePermission::GetEffectivePermission
author: windows-sdk-content
description: Returns the effective permission for an object type.
old-location: security\ieffectivepermission_geteffectivepermission.htm
tech.root: SecAuthZ
ms.assetid: fef2dfe0-3c56-4502-9e8d-900aea84318b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetEffectivePermission, GetEffectivePermission method [Security], GetEffectivePermission method [Security],IEffectivePermission interface, IEffectivePermission interface [Security],GetEffectivePermission method, IEffectivePermission.GetEffectivePermission, IEffectivePermission::GetEffectivePermission, aclui/IEffectivePermission::GetEffectivePermission, security.ieffectivepermission_geteffectivepermission
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: aclui.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Aclui.h
api_name:
 - IEffectivePermission.GetEffectivePermission
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEffectivePermission::GetEffectivePermission


## -description


The <b>GetEffectivePermission</b> method returns the effective permission for an object type.


## -parameters




### -param pguidObjectType [in]

A <b>GUID</b> for the object type whose permission is being queried.


### -param pUserSid [in]

A pointer to a <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that represents the security principal whose effective permission is being determined.


### -param pszServerName [in]

A pointer to null-terminated wide character string that represents the server name.


### -param pSD [in]

A pointer to a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that represents the object's  <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. The security descriptor is used to perform the access check.


### -param ppObjectTypeList [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/c729ff1a-65f3-4f6f-84dd-5700aead75ce">OBJECT_TYPE_LIST</a> structure that represents the array of object types in the object tree for the object. If an object does not support property access, use the following technique to specify the value for the <b>OBJECT_TYPE_LIST</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;

OBJECT_TYPE_LIST g_DefaultOTL[] = {
 {0, 0, (LPGUID)&amp;GUID_NULL},
};

</pre>
</td>
</tr>
</table></span></div>

### -param pcObjectTypeListLength [out]

A pointer to a <b>ULONG</b> that receives the count of object types pointed to by  <i>ppObjectTypeList</i>.


### -param ppGrantedAccessList [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> that receives the array of granted access masks. The operating system will use <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to free the memory allocated for this parameter.


### -param pcGrantedAccessListLength [out]

A pointer to a <b>ULONG</b> variable that receives the count of granted access masks pointed to by  the <i>ppGrantedAccessList</i> parameter.


## -returns



If the function is successful, the return value is S_OK.

If the function fails, the return value is an <b>HRESULT</b> that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



