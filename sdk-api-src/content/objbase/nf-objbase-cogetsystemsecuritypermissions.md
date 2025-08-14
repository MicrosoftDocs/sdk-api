---
UID: NF:objbase.CoGetSystemSecurityPermissions
title: CoGetSystemSecurityPermissions function (objbase.h)
description: Returns the default values of the Security Descriptors of the machine-wide launch and access permissions, as well as launch and access limits.
helpviewer_keywords: ["CoGetSystemSecurityPermissions","CoGetSystemSecurityPermissions function [COM]","com.cogetsystemsecuritypermissions","objbase/CoGetSystemSecurityPermissions"]
old-location: com\cogetsystemsecuritypermissions.htm
tech.root: com
ms.assetid: 8210A6A0-B861-4E85-8E5A-1BF82A01C54E
ms.date: 12/05/2018
ms.keywords: CoGetSystemSecurityPermissions, CoGetSystemSecurityPermissions function [COM], com.cogetsystemsecuritypermissions, objbase/CoGetSystemSecurityPermissions
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoGetSystemSecurityPermissions
 - objbase/CoGetSystemSecurityPermissions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-private-l1-3-1.dll
 - api-ms-win-core-com-private-l1-3-0.dll
 - api-ms-win-core-com-private-l1-2-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-private-l1-1-0.dll
 - API-MS-Win-Core-COM-Private-l1-1-1.dll
api_name:
 - CoGetSystemSecurityPermissions
---

# CoGetSystemSecurityPermissions function


## -description

Returns the default values of the Security Descriptors of the machine-wide launch and access permissions, as well as launch and access limits.

## -parameters

### -param comSDType [in]

A value from the <a href="/windows/desktop/api/objbase/ne-objbase-comsd">COMSD</a> enumeration. Specifies the type of the requested system security permissions, such as launch permissions, access permissions, launch restrictions, and access restrictions.

### -param ppSD [out]

Pointer to a caller-supplied variable that this routine sets to the address of a buffer containing the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> for the system security permissions. Memory will be allocated by <b>CoGetSystemSecurityPermissions</b> and should be freed by caller with <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

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

<a href="/windows/desktop/api/objbase/ne-objbase-comsd">COMSD</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>