---
UID: NF:ntmsapi.GetNtmsObjectAttributeA
title: GetNtmsObjectAttributeA function (ntmsapi.h)
description: The GetNtmsObjectAttribute function retrieves the extended attribute (named private data) from the specified RSM object. (ANSI)
helpviewer_keywords: ["GetNtmsObjectAttributeA", "ntmsapi/GetNtmsObjectAttributeA"]
old-location: fs\getntmsobjectattribute.htm
tech.root: fs
ms.assetid: 9a92d60c-a25f-4775-adb9-1a02af3c8917
ms.date: 12/05/2018
ms.keywords: GetNtmsObjectAttribute, GetNtmsObjectAttribute function [Files], GetNtmsObjectAttributeA, GetNtmsObjectAttributeW, _zaw_getntmsobjectattribute, base.getntmsobjectattribute, fs.getntmsobjectattribute, ntmsapi/GetNtmsObjectAttribute, ntmsapi/GetNtmsObjectAttributeA, ntmsapi/GetNtmsObjectAttributeW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNtmsObjectAttributeW (Unicode) and GetNtmsObjectAttributeA (ANSI)
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
 - GetNtmsObjectAttributeA
 - ntmsapi/GetNtmsObjectAttributeA
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
 - GetNtmsObjectAttribute
 - GetNtmsObjectAttributeA
 - GetNtmsObjectAttributeW
---

# GetNtmsObjectAttributeA function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetNtmsObjectAttribute</b> function retrieves the extended attribute (named private data) from the specified RSM object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

Unique identifier of the object from which to retrieve the data.

### -param dwType [in]

RSM object type. For a list of object types, see 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a>.

### -param lpAttributeName [in]

Name of the extended attribute whose data is to be retrieved.

### -param lpAttributeData [out]

Pointer to the buffer that receives the data.

### -param lpAttributeSize [in, out]

Size of the data buffer on input, in bytes. On output, the actual size of the data, in bytes.

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
 NTMS_USE_ACCESS to the object or its container is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
The database query or update failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size is not correctly specified. The correct size is returned in the <i>lpAttributeSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The pointer is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified attribute was not found.

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

The 
<b>GetNtmsObjectAttribute</b> function must be executed on the RSM server. Because the buffer of bytes is unmarshaled between systems of different architectures, remote execution of this function may result in unpredictable results.

The following is the list of objects that require special access rights.

<table>
<tr>
<th>Object</th>
<th>Access</th>
</tr>
<tr>
<td>NTMS_CHANGER</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_CHANGER_TYPE</td>
<td>Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_COMPUTER</td>
<td>Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_DRIVE</td>
<td>Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_DRIVE_TYPE</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_IEDOOR</td>
<td>Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_IEPORT</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LIBRARY</td>
<td> Requires NTMS_USE_ACCESS to the library.
						</td>
</tr>
<tr>
<td>NTMS_LIBREQUEST</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LOGICAL_MEDIA</td>
<td> Requires NTMS_USE_ACCESS to the media pool of the logical media.
						</td>
</tr>
<tr>
<td>NTMS_MEDIA_POOL</td>
<td>Requires NTMS_USE_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_MEDIA_TYPE</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_OPREQUEST</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_PARTITION</td>
<td> Requires NTMS_USE_ACCESS to the media pool of the side.
						</td>
</tr>
<tr>
<td>NTMS_PHYSICAL_MEDIA</td>
<td> Requires NTMS_USE_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_STORAGESLOT</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
</table>
 





> [!NOTE]
> The ntmsapi.h header defines GetNtmsObjectAttribute as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectattributea">SetNtmsObjectAttribute</a>
