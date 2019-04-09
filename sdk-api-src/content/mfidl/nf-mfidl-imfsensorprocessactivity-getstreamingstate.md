---
UID: NF:mfidl.IMFSensorProcessActivity.GetStreamingState
title: IMFSensorProcessActivity::GetStreamingState (mfidl.h)
author: windows-sdk-content
description: Gets a value indicating whether the sensor is currently streaming.
old-location: mf\imfsensorprocessactivity_getstreamingstate.htm
tech.root: medfound
ms.assetid: C8A99D4B-F3D5-41D2-A956-C147900F28ED
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetStreamingState, GetStreamingState method [Media Foundation], GetStreamingState method [Media Foundation],IMFSensorProcessActivity interface, IMFSensorProcessActivity interface [Media Foundation],GetStreamingState method, IMFSensorProcessActivity.GetStreamingState, IMFSensorProcessActivity::GetStreamingState, mf.imfsensorprocessactivity_getstreamingstate, mfidl/IMFSensorProcessActivity::GetStreamingState
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a>
 

 

