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

# IWMCodecInfo::GetCodecInfoCount


## -description



The <b>GetCodecInfoCount</b> method retrieves the number of supported codecs for a specified major type of digital media (audio or video).




## -parameters




### -param guidType [in]

<b>GUID</b> identifying the major type of digital media. This must be one of the following constants.

<table>
<tr>
<th>
                  Constant
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>WMMEDIATYPE_Video</td>
<td>Specifies a video codec.</td>
</tr>
<tr>
<td>WMMEDIATYPE_Audio</td>
<td>Specifies an audio codec.</td>
</tr>
</table>
 


### -param pcCodecs [out]

Pointer to a count of supported codecs.


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
<i>pcCodecs</i> has been passed a null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>guidType</i> is not a type for which codecs are used.

</td>
</tr>
</table>
 




## -remarks



Use this method along with <b>GetCodecFormatCount</b> and <b>GetCodecFormat</b> to enumerate through the supported codecs for each media type, and the supported formats for each codec.

The Windows Media Format SDK provides codecs only for audio and video. If you specify another major type, this method will return an error.




## -see-also




<a href="https://msdn.microsoft.com/70661d13-737a-4e83-94e6-9a1af07b0369">IWMCodecInfo Interface</a>



<a href="https://msdn.microsoft.com/dbfffc96-2286-4fdf-a76f-ad8e0ecd7aff">IWMCodecInfo::GetCodecFormat</a>



<a href="https://msdn.microsoft.com/b93bfb01-4179-4a0b-bca0-92b1a9a8e605">IWMCodecInfo::GetCodecFormatCount</a>
 

 

