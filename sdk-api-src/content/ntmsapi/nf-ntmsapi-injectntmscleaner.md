---
UID: NF:ntmsapi.InjectNtmsCleaner
title: InjectNtmsCleaner function (ntmsapi.h)
description: The InjectNtmsCleaner function allows a cleaner cartridge to be inserted into the specified library unit.
helpviewer_keywords: ["InjectNtmsCleaner","InjectNtmsCleaner function [Files]","NTMS_INJECT_START","NTMS_INJECT_STOP","_zaw_injectntmscleaner","base.injectntmscleaner","fs.injectntmscleaner","ntmsapi/InjectNtmsCleaner"]
old-location: fs\injectntmscleaner.htm
tech.root: fs
ms.assetid: 973441cb-2ec4-4a8d-8e75-3c6d01552a59
ms.date: 12/05/2018
ms.keywords: InjectNtmsCleaner, InjectNtmsCleaner function [Files], NTMS_INJECT_START, NTMS_INJECT_STOP, _zaw_injectntmscleaner, base.injectntmscleaner, fs.injectntmscleaner, ntmsapi/InjectNtmsCleaner
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
 - InjectNtmsCleaner
 - ntmsapi/InjectNtmsCleaner
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
 - InjectNtmsCleaner
---

# InjectNtmsCleaner function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>InjectNtmsCleaner</b> function allows a cleaner cartridge to be inserted into the specified library unit.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpLibrary [in]

Unique identifier of a library object.

### -param lpInjectOperation [in, out]

GUID of the insert process library operation. If <i>dwAction</i> is NTMS_INJECT_START, this parameter receives the GUID for the operation. If <i>dwAction</i> is NTMS_INJECT_STOP, this parameter must be set to the GUID for the operation to be stopped.

### -param dwNumberOfCleansLeft [out]

Number of cleaning cycles left on the inserted cleaning cartridge.

### -param dwAction [in]

This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_INJECT_START"></a><a id="ntms_inject_start"></a><dl>
<dt><b>NTMS_INJECT_START</b></dt>
</dl>
</td>
<td width="60%">
Start the insertion with either the NTMS_IEPORT or the NTMS_IEDOOR object. A single cleaner cartridge should be inserted. If the NTMS_IEDOOR object is used, no inventory will be performed on the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_INJECT_STOP"></a><a id="ntms_inject_stop"></a><dl>
<dt><b>NTMS_INJECT_STOP</b></dt>
</dl>
</td>
<td width="60%">
Terminates the insertion prior to the time-out event lapsing. (For libraries with ports only.)

</td>
</tr>
</table>

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
Access to at least one RSM object is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The library is not currently connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
Unable to retrieve the library definition from the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_LIBRARY_OFFLINE</b></dt>
</dl>
</td>
<td width="60%">
The library must be online for a cleaner cartridge to be inserted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SLOT_SET</b></dt>
</dl>
</td>
<td width="60%">
This library has no slot reserved as a cleaner slot.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_FULL</b></dt>
</dl>
</td>
<td width="60%">
A cleaner slot is reserved but already has a cleaner cartridge. The cleaner cartridge must be ejected first, using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmscleaner">EjectNtmsCleaner</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
A cleaner slot is reserved but the slot specified is currently not installed in the library. This error occurs if at least one magazine is missing from the library.

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

This function returns to the application as soon as the insert request is queued.

To use the 
<b>InjectNtmsCleaner</b> function, the number of cleaning cycles that remain on the cleaner cartridge must be specified so that RSM can keep track of it.

If an NTMS_IEPORT object is available, the NTMS_IEPORT object directs the cartridge to the currently reserved cleaner slot.

If there is no NTMS_IEPORT object, a door access is performed. In this case, the operator is directed to place the media into the reserved slot.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cleanntmsdrive">CleanNtmsDrive</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Cleaner Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmscleaner">EjectNtmsCleaner</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-releasentmscleanerslot">ReleaseNtmsCleanerSlot</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-reserventmscleanerslot">ReserveNtmsCleanerSlot</a>