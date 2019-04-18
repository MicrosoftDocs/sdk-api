---
UID: NF:ntmsapi.SetNtmsDeviceChangeDetection
title: SetNtmsDeviceChangeDetection function (ntmsapi.h)
author: windows-sdk-content
description: The SetNtmsDeviceChangeDetection function sets one or more target devices for change detection.
old-location: fs\setntmsdevicechangedetection.htm
tech.root: Rsm
ms.assetid: 803bd7d6-f098-42f1-83da-fe9f71f960b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetNtmsDeviceChangeDetection, SetNtmsDeviceChangeDetection function [Files], _zaw_setntmsdevicechangedetection, base.setntmsdevicechangedetection, fs.setntmsdevicechangedetection, ntmsapi/SetNtmsDeviceChangeDetection
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - SetNtmsDeviceChangeDetection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetNtmsDeviceChangeDetection function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsDeviceChangeDetection</b> function sets one or more target devices for change detection.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param DetectHandle [in]

Device change detection handle from 
<a href="https://msdn.microsoft.com/d325a10a-5bf9-4431-8a6a-a50c4cf46728">BeginNtmsDeviceChangeDetection</a>, or <b>NULL</b> for a single poll.


### -param lpRequestId [in]

Object identifier for the target device. This parameter can be one or more library, media type, or physical media GUIDs. All GUIDs must be the same type.


### -param dwType [in]

Type of object identifiers specified in the <i>lpObjectId</i> parameter. This parameter can be one of the following values from the 
<a href="https://msdn.microsoft.com/598e7cb1-f463-4252-9bdf-ccb98f36f4da">NtmsObjectsTypes</a> enumeration type: NTMS_LIBRARY, NTMS_MEDIA_TYPE, or NTMS_PHYSICAL_MEDIA.


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
<a href="https://msdn.microsoft.com/cb8dc379-30a1-43b0-b5a7-c6bc59b3e9ac">EndNtmsDeviceChangeDetection</a> function.

This function can also be used to poll for changed media in the specified devices. This is typically used by a UI when opening a leaf node or implementing a refresh option.




## -see-also




<a href="https://msdn.microsoft.com/d325a10a-5bf9-4431-8a6a-a50c4cf46728">BeginNtmsDeviceChangeDetection</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Change Detection Functions</a>



<a href="https://msdn.microsoft.com/cb8dc379-30a1-43b0-b5a7-c6bc59b3e9ac">EndNtmsDeviceChangeDetection</a>
 

 

