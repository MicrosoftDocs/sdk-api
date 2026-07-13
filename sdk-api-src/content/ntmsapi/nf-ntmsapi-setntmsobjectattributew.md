---
UID: NF:ntmsapi.SetNtmsObjectAttributeW
title: SetNtmsObjectAttributeW function (ntmsapi.h)
description: The SetNtmsObjectAttribute function creates an extended attribute (named private data) in the specified RSM object. (Unicode)
helpviewer_keywords: ["SetNtmsObjectAttribute", "SetNtmsObjectAttribute function [Files]", "SetNtmsObjectAttributeW", "_zaw_setntmsobjectattribute", "base.setntmsobjectattribute", "fs.setntmsobjectattribute", "ntmsapi/SetNtmsObjectAttribute", "ntmsapi/SetNtmsObjectAttributeW"]
old-location: fs\setntmsobjectattribute.htm
tech.root: fs
ms.assetid: ce572b2a-f4c3-4cf3-8bb3-074ba3d1ec30
ms.date: 12/05/2018
ms.keywords: SetNtmsObjectAttribute, SetNtmsObjectAttribute function [Files], SetNtmsObjectAttributeA, SetNtmsObjectAttributeW, _zaw_setntmsobjectattribute, base.setntmsobjectattribute, fs.setntmsobjectattribute, ntmsapi/SetNtmsObjectAttribute, ntmsapi/SetNtmsObjectAttributeA, ntmsapi/SetNtmsObjectAttributeW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetNtmsObjectAttributeW (Unicode) and SetNtmsObjectAttributeA (ANSI)
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
 - SetNtmsObjectAttributeW
 - ntmsapi/SetNtmsObjectAttributeW
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
 - SetNtmsObjectAttribute
 - SetNtmsObjectAttributeA
 - SetNtmsObjectAttributeW
---

# SetNtmsObjectAttributeW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsObjectAttribute</b> function creates an extended attribute (named private data) in the specified RSM object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

GUID of the RSM object for which the extended attribute is to be created.

### -param dwType [in]

RSM object type. For a list of object types, see 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a>.

### -param lpAttributeName [in]

Name of the extended attribute to be created.

### -param lpAttributeData [in]

User-defined data.

### -param AttributeSize

Size of the <i>lpAttributeData</i> buffer, in bytes.D



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
 NTMS_MODIFY_ACCESS is denied to the object or no modifications are allowed for the specified object type (see Remarks). Other security errors are also possible, but they would indicate a security subsystem error.

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
The database update failed.

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
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name or attribute is not valid. The NTMS_MAXATTR_NAMELEN value defines the maximum attribute name length. The length includes a <b>NULL</b>.

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
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
The attribute specified is greater than or equal to NTMS_MAXATTR_LENGTH.

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
The GUID is not valid.

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
<b>SetNtmsObjectAttribute</b> function must be executed on the specified RSM server. Because the buffer of bytes is unmarshaled between systems of different architectures, remote execution of this function can result in unpredictable results.

To delete an attribute, perform a set of the attribute with a length of zero.

The following is the list of objects that require special access rights.

<table>
<tr>
<th>Object</th>
<th>Access</th>
</tr>
<tr>
<td>NTMS_CHANGER</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_CHANGER_TYPE</td>
<td>Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_COMPUTER</td>
<td>Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_DRIVE</td>
<td>Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_DRIVE_TYPE</td>
<td> Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_IEDOOR</td>
<td>Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_IEPORT</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LIBRARY</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.
						</td>
</tr>
<tr>
<td>NTMS_LIBREQUEST</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LOGICAL_MEDIA</td>
<td> Requires NTMS_MODIFY_ACCESS to the media pool of the logical media.
						</td>
</tr>
<tr>
<td>NTMS_MEDIA_POOL</td>
<td>Requires NTMS_MODIFY_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_MEDIA_TYPE</td>
<td> Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_OPREQUEST</td>
<td> Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_PARTITION</td>
<td> Requires NTMS_MODIFY_ACCESS to the media pool of the side.
						</td>
</tr>
<tr>
<td>NTMS_PHYSICAL_MEDIA</td>
<td> Requires NTMS_MODIFY_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_STORAGESLOT</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
</table>
 





> [!NOTE]
> The ntmsapi.h header defines SetNtmsObjectAttribute as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectattributea">GetNtmsObjectAttribute</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>
