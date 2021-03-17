---
UID: NF:ntmsapi.SetNtmsObjectSecurity
title: SetNtmsObjectSecurity function (ntmsapi.h)
description: The SetNtmsObjectSecurity function writes the security descriptor for the specified RSM object.
helpviewer_keywords: ["SetNtmsObjectSecurity","SetNtmsObjectSecurity function [Files]","_zaw_setntmsobjectsecurity","base.setntmsobjectsecurity","fs.setntmsobjectsecurity","ntmsapi/SetNtmsObjectSecurity"]
old-location: fs\setntmsobjectsecurity.htm
tech.root: fs
ms.assetid: ea6be316-6188-46a2-b12a-fe8426bc5fac
ms.date: 12/05/2018
ms.keywords: SetNtmsObjectSecurity, SetNtmsObjectSecurity function [Files], _zaw_setntmsobjectsecurity, base.setntmsobjectsecurity, fs.setntmsobjectsecurity, ntmsapi/SetNtmsObjectSecurity
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
 - SetNtmsObjectSecurity
 - ntmsapi/SetNtmsObjectSecurity
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
 - SetNtmsObjectSecurity
---

# SetNtmsObjectSecurity function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsObjectSecurity</b> function writes the security descriptor for the specified RSM object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

Unique identifier of the RSM object.

### -param dwType [in]

RSM object type. For a list of object types, see the 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a>.

### -param SecurityInformation [in]

A 
<a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> value that specifies the security information to write to the RSM object.

### -param lpSecurityDescriptor [in]

Pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that specifies the security descriptor to write to the RSM object: NTMS_USE_ACCESS, NTMS_CONTROL_ACCESS, or NTMS_MODIFY_ACCESS.

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
The privileges required to modify the security descriptor are denied.

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
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

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

If an application uses 
<b>SetNtmsObjectSecurity</b> to set the discretionary access-control list (ACL) of an object, the application must have WRITE_DAC permission or be the owner of the object.

If an application uses 
<b>SetNtmsObjectSecurity</b> to set the system ACL of an object, the SE_SECURITY_NAME privilege must be enabled for the application. For more information, see the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a> function. For more information on RSM security, see 
<a href="/previous-versions/windows/desktop/rsm/rsm-security">RSM Security</a>.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectsecurity">GetNtmsObjectSecurity</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>