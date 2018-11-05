---
UID: NF:objbase.CoGetSystemSecurityPermissions
title: CoGetSystemSecurityPermissions function
author: windows-sdk-content
description: Returns the default values of the Security Descriptors of the machine-wide launch and access permissions, as well as launch and access limits.
old-location: com\cogetsystemsecuritypermissions.htm
tech.root: com
ms.assetid: 8210A6A0-B861-4E85-8E5A-1BF82A01C54E
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CoGetSystemSecurityPermissions, CoGetSystemSecurityPermissions function [COM], com.cogetsystemsecuritypermissions, objbase/CoGetSystemSecurityPermissions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: ComBase.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoGetSystemSecurityPermissions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoGetSystemSecurityPermissions function


## -description


Returns the default values of the Security Descriptors of the machine-wide launch and access permissions, as well as launch and access limits.


## -parameters




### -param comSDType [in]

A value from the <a href="https://msdn.microsoft.com/FF783F27-D5EF-4927-9B7D-489271FBA9B3">COMSD</a> enumeration. Specifies the type of the requested system security permissions, such as launch permissions, access permissions, launch restrictions, and access restrictions.


### -param ppSD [out]

Pointer to a caller-supplied variable that this routine sets to the address of a buffer containing the <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> for the system security permissions. Memory will be allocated by <b>CoGetSystemSecurityPermissions</b> and should be freed by caller with <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter <i>comSDType</i> or <i>ppSD</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
No connection to the resolver process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory for the security descriptor's allocation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/FF783F27-D5EF-4927-9B7D-489271FBA9B3">COMSD</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

