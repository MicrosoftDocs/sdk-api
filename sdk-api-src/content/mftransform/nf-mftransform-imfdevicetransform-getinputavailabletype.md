---
UID: NF:mftransform.IMFDeviceTransform.GetInputAvailableType
title: IMFDeviceTransform::GetInputAvailableType (mftransform.h)
author: windows-sdk-content
description: The GetInputAvailableType method gets an available media type for an input stream on this Media Foundation transform (MFT).
old-location: stream\imfdevicetransform_getinputavailabletype.htm
tech.root: stream
ms.assetid: 7F3DA67A-AC31-43A5-83AF-7744F6AA5810
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInputAvailableType, GetInputAvailableType method [Streaming Media Devices], GetInputAvailableType method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetInputAvailableType method, IMFDeviceTransform.GetInputAvailableType, IMFDeviceTransform::GetInputAvailableType, mftransform/IMFDeviceTransform::GetInputAvailableType, stream.imfdevicetransform_getinputavailabletype
ms.topic: method
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
 - IMFDeviceTransform.GetInputAvailableType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFDeviceTransform::GetInputAvailableType


## -description


The <b>GetInputAvailableType</b> method gets an available media type for an input stream on this Media Foundation transform (MFT).


## -parameters




### -param dwInputStreamID [in]

Input stream identifier. To get the list of stream identifiers, call <a href="https://msdn.microsoft.com/378A8E3F-8B1E-4C0B-9C30-FE78E1939422">IMFDeviceTransform::GetStreamID</a>.


### -param dwTypeIndex [in]

Index of the media type to retrieve. Media types are indexed from zero and returned in approximate order of preference.


### -param pMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface.


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
Initialization succeeded

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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
There is no media type available with the specified index.

</td>
</tr>
</table>
 




## -remarks



The MFT defines a list of available media types for each input stream and orders them by preference. This method enumerates the available media types for an input stream. To enumerate the available types, increment <i>dwTypeIndex</i> until the method returns <b>MF_E_NO_MORE_TYPES</b>.

<h3><a id="Implementation_notes"></a><a id="implementation_notes"></a><a id="IMPLEMENTATION_NOTES"></a>Implementation notes</h3>
If the MFT stores a media type internally, the MFT should return a clone of the media type, not a pointer to the original type. Otherwise, the caller might modify the type and alter the internal state of the MFT.




## -see-also




<a href="https://msdn.microsoft.com/375293FA-8017-4F74-A93C-C15FED8F19AF">IMFDeviceTransform</a>
 

 

