---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# IShellImageData::Scale


## -description


Adjusts the size of an image.


## -parameters




### -param cx [in]

Type: <b>ULONG</b>

The horizontal (x) dimension. If this value is 0, the x dimension is set to a scaled value based on the point specified in <i>cy</i>.


### -param cy [in]

Type: <b>ULONG</b>

The vertical (y) dimension. If this value is 0, the y dimension is set to a scaled value based on the point specified in <i>cx</i>.


### -param hints [in]

Type: <b><a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a></b>

A member of the <a href="https://msdn.microsoft.com/a74250f7-7939-49a9-bf64-5a97913a4c5b">InterpolationMode</a> enumeration, specifying the algorithm that is used when the image is scaled.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The image was not previously decoded or the call to <a href="https://msdn.microsoft.com/954424d6-cb90-46c1-a850-4e1113dfe2e4">IShellImageData::Decode</a> failed. Other internal calls also can cause this error to be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTVALIDFORANIMATEDIMAGE</b></dt>
</dl>
</td>
<td width="60%">
The image is an animated image and cannot be scaled using this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The internal object cannot be instantiated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The process was stopped by the calling application through a registered instance of <a href="https://msdn.microsoft.com/98a79c41-a384-4486-af51-a33cd5f0750e">IShellImageDataAbort</a>.

</td>
</tr>
</table>
 



