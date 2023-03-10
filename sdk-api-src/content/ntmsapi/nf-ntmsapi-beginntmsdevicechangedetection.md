---
UID: NF:ntmsapi.BeginNtmsDeviceChangeDetection
title: BeginNtmsDeviceChangeDetection function (ntmsapi.h)
description: The BeginNtmsDeviceChangeDetection function allows the application to begin a device change detection session.
helpviewer_keywords: ["BeginNtmsDeviceChangeDetection","BeginNtmsDeviceChangeDetection function [Files]","_zaw_beginntmsdevicechangedetection","base.beginntmsdevicechangedetection","fs.beginntmsdevicechangedetection","ntmsapi/BeginNtmsDeviceChangeDetection"]
old-location: fs\beginntmsdevicechangedetection.htm
tech.root: fs
ms.assetid: d325a10a-5bf9-4431-8a6a-a50c4cf46728
ms.date: 12/05/2018
ms.keywords: BeginNtmsDeviceChangeDetection, BeginNtmsDeviceChangeDetection function [Files], _zaw_beginntmsdevicechangedetection, base.beginntmsdevicechangedetection, fs.beginntmsdevicechangedetection, ntmsapi/BeginNtmsDeviceChangeDetection
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
 - BeginNtmsDeviceChangeDetection
 - ntmsapi/BeginNtmsDeviceChangeDetection
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
 - BeginNtmsDeviceChangeDetection
---

# BeginNtmsDeviceChangeDetection function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>BeginNtmsDeviceChangeDetection</b> function allows the application to begin a device change detection session.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpDetectHandle [out]

Pointer to variable that receives the device change detection handle.

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
The value of the <i>hSession</i> parameter is not a valid session handle.

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

After calling 
<b>BeginNtmsDeviceChangeDetection</b>, the application can set the stand-alone libraries for which media change detection is required using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsdevicechangedetection">SetNtmsDeviceChangeDetection</a> function. The Removable Storage Manager continues to detect changes for the devices specified until the change detection session is closed using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-endntmsdevicechangedetection">EndNtmsDeviceChangeDetection</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Change Detection Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-endntmsdevicechangedetection">EndNtmsDeviceChangeDetection</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsdevicechangedetection">SetNtmsDeviceChangeDetection</a>