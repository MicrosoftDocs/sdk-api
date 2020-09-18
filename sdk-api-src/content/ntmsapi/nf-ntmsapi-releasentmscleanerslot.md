---
UID: NF:ntmsapi.ReleaseNtmsCleanerSlot
title: ReleaseNtmsCleanerSlot function (ntmsapi.h)
description: The ReleaseNtmsCleanerSlot function removes an existing slot reservation for a cleaning cartridge. The slot can then be used for data cartridges.
helpviewer_keywords: ["ReleaseNtmsCleanerSlot","ReleaseNtmsCleanerSlot function [Files]","_zaw_releasentmscleanerslot","base.releasentmscleanerslot","fs.releasentmscleanerslot","ntmsapi/ReleaseNtmsCleanerSlot"]
old-location: fs\releasentmscleanerslot.htm
tech.root: fs
ms.assetid: c3530534-c502-4168-8039-b5ce4f0a5816
ms.date: 12/05/2018
ms.keywords: ReleaseNtmsCleanerSlot, ReleaseNtmsCleanerSlot function [Files], _zaw_releasentmscleanerslot, base.releasentmscleanerslot, fs.releasentmscleanerslot, ntmsapi/ReleaseNtmsCleanerSlot
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
 - ReleaseNtmsCleanerSlot
 - ntmsapi/ReleaseNtmsCleanerSlot
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
 - ReleaseNtmsCleanerSlot
---

# ReleaseNtmsCleanerSlot function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ReleaseNtmsCleanerSlot</b> function removes an existing slot reservation for a cleaning cartridge. The slot can then be used for data cartridges.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpLibrary [in]

Unique identifier of the library to release the cleaner slot.

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
NTMS_CONTROL_ACCESS to the library is denied. Other security errors are also possible, but they would indicate a security subsystem error.

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
<dt><b>ERROR_NO_SLOT_RESERVED</b></dt>
</dl>
</td>
<td width="60%">
This library has no slot reserved for a cleaner cartridge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_FULL</b></dt>
</dl>
</td>
<td width="60%">
The library has a reserved cleaner cartridge slot but the slot contains a cleaner cartridge (the slot must be empty). Use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmscleaner">EjectNtmsCleaner</a> function to eject a cleaner cartridge.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The library has a reserved cleaner cartridge slot, but the specified slot is currently not installed in the library. This error can occur if at least one magazine is missing from the library.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was queued successfully.

</td>
</tr>
</table>

## -remarks

For the 
<b>ReleaseNtmsCleanerSlot</b> function to succeed, the slot must be present and empty. The library must also have a slot reserved for cleaning.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cleanntmsdrive">CleanNtmsDrive</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Cleaner Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-ejectntmscleaner">EjectNtmsCleaner</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-injectntmscleaner">InjectNtmsCleaner</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-reserventmscleanerslot">ReserveNtmsCleanerSlot</a>