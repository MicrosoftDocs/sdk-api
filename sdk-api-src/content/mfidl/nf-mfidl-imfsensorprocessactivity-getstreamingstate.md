---
UID: NF:mfidl.IMFSensorProcessActivity.GetStreamingState
title: IMFSensorProcessActivity::GetStreamingState (mfidl.h)
description: Gets a value indicating whether the sensor is currently streaming.
helpviewer_keywords: ["GetStreamingState","GetStreamingState method [Media Foundation]","GetStreamingState method [Media Foundation]","IMFSensorProcessActivity interface","IMFSensorProcessActivity interface [Media Foundation]","GetStreamingState method","IMFSensorProcessActivity.GetStreamingState","IMFSensorProcessActivity::GetStreamingState","mf.imfsensorprocessactivity_getstreamingstate","mfidl/IMFSensorProcessActivity::GetStreamingState"]
old-location: mf\imfsensorprocessactivity_getstreamingstate.htm
tech.root: mf
ms.assetid: C8A99D4B-F3D5-41D2-A956-C147900F28ED
ms.date: 12/05/2018
ms.keywords: GetStreamingState, GetStreamingState method [Media Foundation], GetStreamingState method [Media Foundation],IMFSensorProcessActivity interface, IMFSensorProcessActivity interface [Media Foundation],GetStreamingState method, IMFSensorProcessActivity.GetStreamingState, IMFSensorProcessActivity::GetStreamingState, mf.imfsensorprocessactivity_getstreamingstate, mfidl/IMFSensorProcessActivity::GetStreamingState
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorProcessActivity::GetStreamingState
 - mfidl/IMFSensorProcessActivity::GetStreamingState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorProcessActivity.GetStreamingState
---

# IMFSensorProcessActivity::GetStreamingState


## -description

Gets a value indicating whether the sensor is currently streaming.

## -parameters

### -param pfStreaming [out]

Receives a value indicating whether the sensor is currently streaming.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfStreaming</i> parameter is null.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a>