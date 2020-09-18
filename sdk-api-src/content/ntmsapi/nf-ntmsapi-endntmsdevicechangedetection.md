---
UID: NF:ntmsapi.EndNtmsDeviceChangeDetection
title: EndNtmsDeviceChangeDetection function (ntmsapi.h)
description: The EndNtmsDeviceChangeDetection function ends device change detection for any target devices specified using the SetNtmsDeviceChangeDetection function and closes the change detection handle.
helpviewer_keywords: ["EndNtmsDeviceChangeDetection","EndNtmsDeviceChangeDetection function [Files]","_zaw_endntmsdevicechangedetection","base.endntmsdevicechangedetection","fs.endntmsdevicechangedetection","ntmsapi/EndNtmsDeviceChangeDetection"]
old-location: fs\endntmsdevicechangedetection.htm
tech.root: fs
ms.assetid: cb8dc379-30a1-43b0-b5a7-c6bc59b3e9ac
ms.date: 12/05/2018
ms.keywords: EndNtmsDeviceChangeDetection, EndNtmsDeviceChangeDetection function [Files], _zaw_endntmsdevicechangedetection, base.endntmsdevicechangedetection, fs.endntmsdevicechangedetection, ntmsapi/EndNtmsDeviceChangeDetection
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
 - EndNtmsDeviceChangeDetection
 - ntmsapi/EndNtmsDeviceChangeDetection
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
 - EndNtmsDeviceChangeDetection
---

# EndNtmsDeviceChangeDetection function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>EndNtmsDeviceChangeDetection</b> function ends device change detection for any target devices specified using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsdevicechangedetection">SetNtmsDeviceChangeDetection</a> function and closes the change detection handle.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function

### -param DetectHandle [in]

Device change detection handle returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-beginntmsdevicechangedetection">BeginNtmsDeviceChangeDetection</a> function.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle or detection handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been canceled.

</td>
</tr>
</table>

## -remarks

Closing the Removable Storage Manager session also ends all device change detection sessions.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-beginntmsdevicechangedetection">BeginNtmsDeviceChangeDetection</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Change Detection Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsdevicechangedetection">SetNtmsDeviceChangeDetection</a>