---
UID: NF:ntmsapi.GetNtmsObjectSecurity
title: GetNtmsObjectSecurity function (ntmsapi.h)
description: The GetNtmsObjectSecurity function reads the security descriptor for the specified RSM object.
helpviewer_keywords: ["GetNtmsObjectSecurity","GetNtmsObjectSecurity function [Files]","_zaw_getntmsobjectsecurity","base.getntmsobjectsecurity","fs.getntmsobjectsecurity","ntmsapi/GetNtmsObjectSecurity"]
old-location: fs\getntmsobjectsecurity.htm
tech.root: fs
ms.assetid: 1d2168a3-077e-48fc-8a06-91952213f2cb
ms.date: 12/05/2018
ms.keywords: GetNtmsObjectSecurity, GetNtmsObjectSecurity function [Files], _zaw_getntmsobjectsecurity, base.getntmsobjectsecurity, fs.getntmsobjectsecurity, ntmsapi/GetNtmsObjectSecurity
req.header: ntmsapi.h
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNtmsObjectSecurity
 - ntmsapi/GetNtmsObjectSecurity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - GetNtmsObjectSecurity
---

# GetNtmsObjectSecurity function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetNtmsObjectSecurity</b> function reads the security descriptor for the specified RSM object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

Unique identifier of the RSM object.

### -param dwType [in]

Object type. For a list of object types, see 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a>.

### -param RequestedInformation [in]

A 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that specifies the requested security data.

### -param lpSecurityDescriptor [out]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that receives the security descriptor.

### -param nLength [in]

Length of the descriptor.

### -param lpnLengthNeeded [out]

Required length of the buffer if it is not large enough for the security descriptor, in bytes.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
 READ_CONTROL access to the object is denied.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The object ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SECURITY_ON_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
There is no security information for this object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The object ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>

## -remarks

RSM security uses the standard security descriptors and information members. This allows the standard security dialog boxes to be used to select RSM security. For more information, see the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a> function. For more information on RSM security, see 
<a href="/previous-versions/windows/desktop/rsm/rsm-security">RSM Security</a>.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectsecurity">SetNtmsObjectSecurity</a>