---
UID: NF:mftransform.IMFDeviceTransform.GetInputStreamState
title: IMFDeviceTransform::GetInputStreamState (mftransform.h)
author: windows-sdk-content
description: The GetInputStreamState method gets the Device MFT’s input stream state.
old-location: stream\imfdevicetransform_getinputstreamstate.htm
tech.root: stream
ms.assetid: B5319512-EC6C-4940-881E-3DB1CA7BF0E3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetInputStreamState, GetInputStreamState method [Streaming Media Devices], GetInputStreamState method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetInputStreamState method, IMFDeviceTransform.GetInputStreamState, IMFDeviceTransform::GetInputStreamState, mftransform/IMFDeviceTransform::GetInputStreamState, stream.imfdevicetransform_getinputstreamstate
ms.topic: method
f1_keywords: 
 - "mftransform/IMFDeviceTransform.GetInputStreamState"
dev_langs:
 - c++
req.header: mftransform.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703
req.target-min-winversvr: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.GetInputStreamState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDeviceTransform::GetInputStreamState


## -description


The  <b>GetInputStreamState</b> method gets the Device MFT’s input stream state.


## -parameters




### -param dwStreamID [in]

Stream ID of the input stream whose state needs to be retrieved.


### -param value [out]

Specifies the current <b>DeviceStreamState</b> of the specified input Device MFT stream. 


## -returns



The method returns an <b>HRESULT</b>. Possible values include but not limited to values given in the following table.

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
Transitioning the stream state succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Device MFT could not  support the request at this time.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVAILIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
An invalid stream ID was passed.

</td>
</tr>
</table>
 




## -remarks



This method is used by device transform  manager (DTM) to get a specific input stream’s state.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransform">IMFDeviceTransform</a>
 

 

