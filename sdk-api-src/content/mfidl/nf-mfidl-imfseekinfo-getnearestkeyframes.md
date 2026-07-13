---
UID: NF:mfidl.IMFSeekInfo.GetNearestKeyFrames
title: IMFSeekInfo::GetNearestKeyFrames (mfidl.h)
description: For a particular seek position, gets the two nearest key frames. (IMFSeekInfo.GetNearestKeyFrames)
helpviewer_keywords: ["GetNearestKeyFrames","GetNearestKeyFrames method [Media Foundation]","GetNearestKeyFrames method [Media Foundation]","IMFSeekInfo interface","IMFSeekInfo interface [Media Foundation]","GetNearestKeyFrames method","IMFSeekInfo.GetNearestKeyFrames","IMFSeekInfo::GetNearestKeyFrames","mf.imfseekinfo_getnearestkeyframes","mfidl/IMFSeekInfo::GetNearestKeyFrames"]
old-location: mf\imfseekinfo_getnearestkeyframes.htm
tech.root: mf
ms.assetid: 72A7161A-09CA-4582-B240-1442D70936D7
ms.date: 12/05/2018
ms.keywords: GetNearestKeyFrames, GetNearestKeyFrames method [Media Foundation], GetNearestKeyFrames method [Media Foundation],IMFSeekInfo interface, IMFSeekInfo interface [Media Foundation],GetNearestKeyFrames method, IMFSeekInfo.GetNearestKeyFrames, IMFSeekInfo::GetNearestKeyFrames, mf.imfseekinfo_getnearestkeyframes, mfidl/IMFSeekInfo::GetNearestKeyFrames
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSeekInfo::GetNearestKeyFrames
 - mfidl/IMFSeekInfo::GetNearestKeyFrames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSeekInfo.GetNearestKeyFrames
---

# IMFSeekInfo::GetNearestKeyFrames


## -description

For a particular seek position, gets the two nearest key frames.

## -parameters

### -param pguidTimeFormat [in]

A pointer to a GUID that specifies the time format. The time format defines the units for the other parameters of this method. If the value is <b>GUID_NULL</b>, the time format is 100-nanosecond units. Some media sources might support additional time format GUIDs.

### -param pvarStartPosition [in]

The seek position. The units for this parameter are specified by <i>pguidTimeFormat</i>.

### -param pvarPreviousKeyFrame [out]

Receives the position of the nearest key frame that appears earlier than <i>pvarStartPosition</i>. The units for this parameter are specified by <i>pguidTimeFormat</i>.

### -param pvarNextKeyFrame [out]

Receives the position of the nearest key frame that appears later than <i>pvarStartPosition</i>. The units for this parameter are specified by <i>pguidTimeFormat</i>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_TIME_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The time format specified in <i>pguidTimeFormat</i> is not supported.

</td>
</tr>
</table>

## -remarks

If an application seeks to a non–key frame, the decoder must start decoding from the previous key frame. This can increase latency, because several frames might get decoded before the requested frame is reached. To reduce latency, an application can call this method to find the two key frames that are closest to the desired time, and then seek to one of those key frames.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfseekinfo">IMFSeekInfo</a>
