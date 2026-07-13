---
UID: NF:ntmsapi.SetNtmsObjectInformationW
title: SetNtmsObjectInformationW function (ntmsapi.h)
description: The SetNtmsObjectInformationW (Unicode) function changes the information structure of the specified object. (SetNtmsObjectInformationW)
helpviewer_keywords: ["SetNtmsObjectInformation", "SetNtmsObjectInformation function [Files]", "SetNtmsObjectInformationW", "_zaw_setntmsobjectinformation", "base.setntmsobjectinformation", "fs.setntmsobjectinformation", "ntmsapi/SetNtmsObjectInformation", "ntmsapi/SetNtmsObjectInformationW"]
old-location: fs\setntmsobjectinformation.htm
tech.root: fs
ms.assetid: 1cdb9c72-1b34-4800-a07d-b648baec8582
ms.date: 08/03/2022
ms.keywords: SetNtmsObjectInformation, SetNtmsObjectInformation function [Files], SetNtmsObjectInformationA, SetNtmsObjectInformationW, _zaw_setntmsobjectinformation, base.setntmsobjectinformation, fs.setntmsobjectinformation, ntmsapi/SetNtmsObjectInformation, ntmsapi/SetNtmsObjectInformationA, ntmsapi/SetNtmsObjectInformationW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetNtmsObjectInformationW (Unicode) and SetNtmsObjectInformationA (ANSI)
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
 - SetNtmsObjectInformationW
 - ntmsapi/SetNtmsObjectInformationW
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
 - SetNtmsObjectInformation
 - SetNtmsObjectInformationA
 - SetNtmsObjectInformationW
---

# SetNtmsObjectInformationW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsObjectInformation</b> function changes the information structure of the specified object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

Unique identifier of the RSM object.

### -param lpInfo [in]

Pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure.

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
NTMS_MODIFY_ACCESS or NTMS_CONTROL_ACCESS is denied to the object being written or no modifications are allowed to the object type specified. See Remarks.

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
The object ID or information structure is missing, or the object information size or object type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An allocation failure occurred during processing.

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
</table>

## -remarks

The information size and type must be set before you can use 
<b>SetNtmsObjectInformation</b>.

All writable properties for the object are read from the 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a> structure and written to the database without regard for any write operations that have occurred between the time this application called the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a> function and the 
<b>SetNtmsObjectInformation</b> function. Because of this you can lose changes.

To avoid unpredictable results, applications must call 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a> before calling 
<b>SetNtmsObjectInformation</b>. As noted above, 
<b>SetNtmsObjectInformation</b> updates all writable members, therefore the application is responsible for providing a value for all writable members.

The following is the list of objects that have members that can be updated.

<table>
<tr>
<th>Object</th>
<th>Members</th>
</tr>
<tr>
<td>NTMS_CHANGER</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the library.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_CHANGER_TYPE</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the computer.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_COMPUTER</td>
<td><b>dwMediaPoolPolicy</b><div> </div><b>dwLibRequestFlags</b><div> </div><b>dwLibRequestPurgeTime</b><div> </div><b>dwOpRequestFlags</b><div> </div><b>dwOpRequestPurgeTime</b><div> </div><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the computer.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_DRIVE</td>
<td><b>dwDeferDismountDelay</b><div> </div><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the library.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_DRIVE_TYPE</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the computer.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_IEDOOR</td>
<td><b>MaxOpenSecs</b><div> </div><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the library.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_IEPORT</td>
<td><b>MaxExtendSecs</b><div> </div><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the library.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_LIBRARY</td>
<td><b>AutoRecovery</b><div> </div><b>dwCleanerUsesRemaining</b><div> </div><b>dwFlags</b><div> </div><b>InventoryMethod</b><div> </div><b>szDescription</b><div> </div><b>szName</b> Requires NTMS_CONTROL_ACCESS to the library.

</td>
</tr>
<tr>
<td>NTMS_LIBREQUEST</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the library.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_LOGICAL_MEDIA</td>
<td><b>szDescription</b><div> </div><b>szName</b> Requires NTMS_MODIFY_ACCESS to the media pool of the logical media.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_MEDIA_POOL</td>
<td><b>AllocationPolicy</b><div> </div><b>DeallocationPolicy</b><div> </div><b>dwMaxAllocates</b><div> </div><b>MediaType</b><div> </div><b>szDescription</b><div> </div><b>szName</b> Requires NTMS_MODIFY_ACCESS to the media pool.

<b>Windows XP:  </b> Requires NTMS_CONTROL_ACCESS to the media pool.

</td>
</tr>
<tr>
<td>NTMS_MEDIA_TYPE</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the computer.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_OPREQUEST</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the computer.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_PARTITION</td>
<td><b>szName</b><div> </div><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the media pool of the side.

<b>Windows XP:  </b> Requires NTMS_CONTROL_ACCESS to the media pool of the side.

</td>
</tr>
<tr>
<td>NTMS_PHYSICAL_MEDIA</td>
<td><b>szDescription</b><div> </div><b>szName</b> Requires NTMS_MODIFY_ACCESS to the media pool.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
<tr>
<td>NTMS_STORAGESLOT</td>
<td><b>szDescription</b> Requires NTMS_MODIFY_ACCESS to the library.

<b>Windows XP:  </b> No access rights are required.

</td>
</tr>
</table>
 





> [!NOTE]
> The ntmsapi.h header defines SetNtmsObjectInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectinformation">GetNtmsObjectInformation</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectsecurity">GetNtmsObjectSecurity</a>



<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_objectinformationa">NTMS_OBJECTINFORMATION</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Object Management Functions</a>
