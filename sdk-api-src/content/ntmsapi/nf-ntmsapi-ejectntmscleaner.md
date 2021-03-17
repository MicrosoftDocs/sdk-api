---
UID: NF:ntmsapi.EjectNtmsCleaner
title: EjectNtmsCleaner function (ntmsapi.h)
description: The EjectNtmsCleaner function ejects the cleaning cartridge from the currently reserved cleaner slot.
helpviewer_keywords: ["EjectNtmsCleaner","EjectNtmsCleaner function [Files]","NTMS_EJECT_START","NTMS_EJECT_STOP","_zaw_ejectntmscleaner","base.ejectntmscleaner","fs.ejectntmscleaner","ntmsapi/EjectNtmsCleaner"]
old-location: fs\ejectntmscleaner.htm
tech.root: fs
ms.assetid: a55a8f17-1a14-4267-ae39-1585e1090f21
ms.date: 12/05/2018
ms.keywords: EjectNtmsCleaner, EjectNtmsCleaner function [Files], NTMS_EJECT_START, NTMS_EJECT_STOP, _zaw_ejectntmscleaner, base.ejectntmscleaner, fs.ejectntmscleaner, ntmsapi/EjectNtmsCleaner
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
 - EjectNtmsCleaner
 - ntmsapi/EjectNtmsCleaner
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
 - EjectNtmsCleaner
---

# EjectNtmsCleaner function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>EjectNtmsCleaner</b> function ejects the cleaning cartridge from the currently reserved cleaner slot.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpLibrary [in]

Unique identifier of a library object.

### -param lpEjectOperation [in, out]

GUID of the eject process library operation. If <i>dwAction</i> is NTMS_EJECT_START, this parameter receives the GUID for the operation. If <i>dwAction</i> is NTMS_EJECT_STOP, this parameter must be set to the GUID for the operation to be stopped.

### -param dwAction [in]

Action to perform. This parameter can be either one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_START"></a><a id="ntms_eject_start"></a><dl>
<dt><b>NTMS_EJECT_START</b></dt>
</dl>
</td>
<td width="60%">
Starts the eject operation with a port. The specified medium is ejected until the time-out event occurs or the function is called again with NTMS_EJECT_STOP. The time-out value is specified in the library object and is applied to all ejections in the library.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_EJECT_STOP"></a><a id="ntms_eject_stop"></a><dl>
<dt><b>NTMS_EJECT_STOP</b></dt>
</dl>
</td>
<td width="60%">
For libraries with NTMS_IEPORT objects only. Terminates the ejection process specified by <i>lpEjectOperation</i> prior to the time-out event lapsing.

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
Access to one or more RSM objects is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value supplied in the <i>hSession</i> parameter is not valid.

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
<dt><b>ERROR_NO_SLOT_SET</b></dt>
</dl>
</td>
<td width="60%">
This library does not have a cleaner slot reserved.

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
<dt><b>ERROR_SLOT_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
A cleaner slot is reserved but is already empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SLOT_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
A cleaner slot is reserved but the slot is currently not installed in the library. This error occurs when at least one magazine is missing from the library.

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
<b>EjectNtmsCleaner</b> function returns to the application as soon as the eject request is queued.

If the library specified in the 
<b>EjectNtmsCleaner</b> function has an NTMS_IEPORT object, RSM uses the NTMS_IEPORT object to eject the cleaner. If there is no NTMS_IEPORT object, the NTMS_IEDOOR object is used to allow the operator to gain access to the cleaner slot.

Ejected cleaner cartridges are not tracked in the offline library.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-cleanntmsdrive">CleanNtmsDrive</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Cleaner Management Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-injectntmscleaner">InjectNtmsCleaner</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-releasentmscleanerslot">ReleaseNtmsCleanerSlot</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-reserventmscleanerslot">ReserveNtmsCleanerSlot</a>