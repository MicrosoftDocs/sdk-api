---
UID: NF:mftransform.IMFDeviceTransform.GetStreamIDs
title: IMFDeviceTransform::GetStreamIDs
author: windows-sdk-content
description: The GetStreamIDs method gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).
old-location: stream\imfdevicetransform_getstreamids.htm
old-project: stream
ms.assetid: 378A8E3F-8B1E-4C0B-9C30-FE78E1939422
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetStreamIDs, GetStreamIDs method [Streaming Media Devices], GetStreamIDs method [Streaming Media Devices],IMFDeviceTransform interface, IMFDeviceTransform interface [Streaming Media Devices],GetStreamIDs method, IMFDeviceTransform.GetStreamIDs, IMFDeviceTransform::GetStreamIDs, mftransform/IMFDeviceTransform::GetStreamIDs, stream.imfdevicetransform_getstreamids
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransform.GetStreamIDs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDeviceTransform::GetStreamIDs


## -description


The  <b>GetStreamIDs</b> method gets the stream identifiers for the input and output streams on this Media Foundation transform (MFT).


## -parameters




### -param dwInputIDArraySize




### -param pdwInputStreamIds




### -param dwOutputIDArraySize




### -param pdwOutputStreamIds






#### - dwInputStreamIDArraySize [in]

The number of elements in <i>pdwInputStreamIDs</i>


#### - dwOutputStreamIDArraySize [out]

The number of elements in <i>pdwOutputStreamIDs</i>.


#### - pdwInputStreamIDs [out]

 A pointer to an array allocated by the caller. The method fills the array with the input stream identifiers. The array size must be at least equal to the number of input streams. To get the number of input streams, call <a href="https://msdn.microsoft.com/6FD4B393-05E6-4400-B1A3-D69B7F1B90F0">IMFDeviceTransform::GetStreamCount</a>. 

If the caller passes an array that is larger than the number of input streams, the MFT must not write values into the extra array entries.


#### - pdwOutputStreamIDs

A pointer to an array allocated by the caller. The method fills the array with the output stream identifiers. The array size must be at least equal to the number of output streams. To get the number of output streams, call <a href="https://msdn.microsoft.com/6FD4B393-05E6-4400-B1A3-D69B7F1B90F0">IMFDeviceTransform::GetStreamCount</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer passed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer coming in does not  have enough space to fill in the stream IDs.

</td>
</tr>
</table>
 




## -remarks



Stream identifiers are necessary because some MFTs can add or remove streams, so the index of a stream may not be unique. Therefore, <a href="https://msdn.microsoft.com/375293FA-8017-4F74-A93C-C15FED8F19AF">IMFDeviceTransform</a> methods that operate on streams take stream identifiers.

All input stream identifiers must be unique within an MFT, and all output stream identifiers must be unique. However, an input stream and an output stream can share the same identifier. 
I

If the client adds an input stream, the client assigns the identifier, so the MFT must allow arbitrary identifiers, as long as they are unique. If the MFT creates an output stream, the MFT assigns the identifier. 


By convention, if an MFT has exactly one fixed input stream and one fixed output stream, it should assign the identifier 0 to both streams.




## -see-also




<a href="https://msdn.microsoft.com/375293FA-8017-4F74-A93C-C15FED8F19AF">IMFDeviceTransform</a>
 

 

