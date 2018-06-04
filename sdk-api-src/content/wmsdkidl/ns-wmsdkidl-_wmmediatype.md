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

# _WMMediaType structure


## -description



The <b>WM_MEDIA_TYPE </b>structure is the primary structure used to describe media formats for the objects of the Windows Media Format SDK. For more information about media formats and what they are used for, see <a href="https://msdn.microsoft.com/7c602643-f1fc-4fbd-a739-4296dc758bc9">Formats</a>.




## -struct-fields




### -field majortype

Major type of the media sample. For example, WMMEDIATYPE_Video specifies a video stream. For a list of possible major media types, see <a href="https://msdn.microsoft.com/00dcbb20-09ed-44c5-992c-20f3d17ad47c">Media Types</a>.


### -field subtype

Subtype of the media sample. The subtype defines a specific format (usually an encoding scheme) within a major media type. For example, WMMEDIASUBTYPE_WMV3 specifies a video stream encoded with the Windows Media Video 9 codec. Subtypes can be uncompressed or compressed. For lists of possible media subtypes, see <a href="https://msdn.microsoft.com/5586e62a-d0f5-45cc-a690-4efa244b3f32">Uncompressed Media Subtypes</a> and <a href="https://msdn.microsoft.com/0ed6b4e8-6450-4484-90d6-efa2f9101782">Compressed Media Subtypes</a>.


### -field bFixedSizeSamples

Set to true if the samples are of a fixed size. Compressed audio samples are of a fixed size while video samples are not.


### -field bTemporalCompression

Set to true if the samples are temporally compressed. Temporal compression is compression where some samples describe the changes in content from the previous sample, instead of describing the sample in its entirety. Only compressed video can be temporally compressed. By definition, no media type can use both fixed sized samples and temporal compression.


### -field lSampleSize

Long integer containing the size of the sample, in bytes. This member is used only if <b>bFixedSizeSamples</b> is true.


### -field formattype

GUID of the format type. The format type specifies the additional structure used to identify the media format. This structure is pointed to by <b>pbFormat</b>.


### -field pUnk

Not used. Should be <b>NULL</b>.


### -field cbFormat

Size, in bytes, of the structure pointed to by pbFormat.


### -field pbFormat

Pointer to the format structure of the media type. The structure referenced is determined by the format type <b>GUID</b>. Format types include:<table>
<tr>
<th>Media Type</th>
<th>Structure</th>
</tr>
<tr>
<td>WMFORMAT_VideoInfo</td>
<td>
<a href="https://msdn.microsoft.com/cf079efd-1759-4787-8aeb-85543847ac44">WMVIDEOINFOHEADER</a>
</td>
</tr>
<tr>
<td>WMFORMAT_WaveFormatEx</td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>
</td>
</tr>
<tr>
<td>WMFORMAT_MPEG2Video</td>
<td>
<a href="https://msdn.microsoft.com/e5907b04-200c-4459-971b-3680989a564f">WMMPEG2VIDEOINFO</a>
</td>
</tr>
<tr>
<td>WMFORMAT_WebStream</td>
<td>
<a href="https://msdn.microsoft.com/3a392b33-6c2b-4465-86b4-6614940d7383">WMT_WEBSTREAM_FORMAT</a>
</td>
</tr>
<tr>
<td>WMFORMAT_Script</td>
<td>
<a href="https://msdn.microsoft.com/b7c513ac-9c28-4556-a0c8-f3e0d6efc735">WMSCRIPTFORMAT</a>
</td>
</tr>
</table>
 




## -remarks



This is the same as the DirectShow structure <b>AM_MEDIA_TYPE</b> but is redefined in this SDK to avoid conflict with DirectShow names.




## -see-also




<a href="https://msdn.microsoft.com/8357e5c6-d8c6-4a30-8446-85fa7fa118f7">IWMMediaProps::GetMediaType</a>



<a href="https://msdn.microsoft.com/7a89bf24-6b76-4645-8f39-f1979029d67e">IWMMediaProps::SetMediaType</a>



<a href="https://msdn.microsoft.com/5d903953-cd6b-4fba-b877-8c7ad3aeb87d">Media Type Identifiers</a>



<a href="https://msdn.microsoft.com/00dcbb20-09ed-44c5-992c-20f3d17ad47c">Media Types</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

