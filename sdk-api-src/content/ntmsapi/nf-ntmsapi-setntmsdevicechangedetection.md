---
UID: NF:ntmsapi.SetNtmsDeviceChangeDetection
title: SetNtmsDeviceChangeDetection function (ntmsapi.h)
description: The SetNtmsDeviceChangeDetection function sets one or more target devices for change detection.
helpviewer_keywords: ["SetNtmsDeviceChangeDetection","SetNtmsDeviceChangeDetection function [Files]","_zaw_setntmsdevicechangedetection","base.setntmsdevicechangedetection","fs.setntmsdevicechangedetection","ntmsapi/SetNtmsDeviceChangeDetection"]
old-location: fs\setntmsdevicechangedetection.htm
tech.root: fs
ms.assetid: 803bd7d6-f098-42f1-83da-fe9f71f960b0
ms.date: 12/05/2018
ms.keywords: SetNtmsDeviceChangeDetection, SetNtmsDeviceChangeDetection function [Files], _zaw_setntmsdevicechangedetection, base.setntmsdevicechangedetection, fs.setntmsdevicechangedetection, ntmsapi/SetNtmsDeviceChangeDetection
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
 - SetNtmsDeviceChangeDetection
 - ntmsapi/SetNtmsDeviceChangeDetection
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
 - SetNtmsDeviceChangeDetection
---

# SetNtmsDeviceChangeDetection function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsDeviceChangeDetection</b> function sets one or more target devices for change detection.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param DetectHandle [in]

Device change detection handle from 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-beginntmsdevicechangedetection">BeginNtmsDeviceChangeDetection</a>, or <b>NULL</b> for a single poll.

### -param lpRequestId [in]

Object identifier for the target device. This parameter can be one or more library, media type, or physical media GUIDs. All GUIDs must be the same type.

### -param dwType [in]

Type of object identifiers specified in the <i>lpObjectId</i> parameter. This parameter can be one of the following values from the 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a> enumeration type: NTMS_LIBRARY, NTMS_MEDIA_TYPE, or NTMS_PHYSICAL_MEDIA.

### -param dwCount [in]

Number of object identifiers in <i>lpObjectId</i>.

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
The session or detection handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The object type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LIBRARY</b></dt>
</dl>
</td>
<td width="60%">
The specified library was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The specified media or type was not found.

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

The device can be specified directly by passing library GUIDs or indirectly by passing physical media or media type GUIDs. When using the indirect specification, all stand-alone libraries that could contain the media or media type are detected. All devices specified continue to be detected until the device change detection handle is closed using the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-endntmsdevicechangedetection">EndNtmsDeviceChangeDetection</a> function.

This function can also be used to poll for changed media in the specified devices. This is typically used by a UI when opening a leaf node or implementing a refresh option.

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-beginntmsdevicechangedetection">BeginNtmsDeviceChangeDetection</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Change Detection Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-endntmsdevicechangedetection">EndNtmsDeviceChangeDetection</a>