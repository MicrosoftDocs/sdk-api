---
UID: NF:mfreadwrite.IMFSourceReader.SetCurrentPosition
title: IMFSourceReader::SetCurrentPosition
author: windows-sdk-content
description: Seeks to a new position in the media source.
old-location: mf\imfsourcereader_setcurrentposition.htm
old-project: medfound
ms.assetid: fb9412f5-4f2f-463d-9988-80e706afd9c4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GUID_NULL, IMFSourceReader interface [Media Foundation],SetCurrentPosition method, IMFSourceReader.SetCurrentPosition, IMFSourceReader::SetCurrentPosition, SetCurrentPosition, SetCurrentPosition method [Media Foundation], SetCurrentPosition method [Media Foundation],IMFSourceReader interface, mf.imfsourcereader_setcurrentposition, mfreadwrite/IMFSourceReader::SetCurrentPosition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: MF_SOURCE_READER_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSourceReader.SetCurrentPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceReader::SetCurrentPosition


## -description


Seeks to a new position in the media source.


## -parameters




### -param guidTimeFormat [in]

A GUID that specifies the <i>time format</i>. The time format defines the units for the <i>varPosition</i> parameter. The following value is defined for all media sources:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_NULL"></a><a id="guid_null"></a><dl>
<dt><b>GUID_NULL</b></dt>
</dl>
</td>
<td width="60%">
100-nanosecond units.

</td>
</tr>
</table>
 

Some media sources might support additional values. 


### -param varPosition [in]

The position from which playback will be started. The units are specified by the <i>guidTimeFormat</i> parameter. If the <i>guidTimeFormat</i> parameter is <b>GUID_NULL</b>, set the variant type to <b>VT_I8</b>.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDREQUEST</b></b></dt>
</dl>
</td>
<td width="60%">
One or more sample requests are still pending.

</td>
</tr>
</table>
 




## -remarks



The <b>SetCurrentPosition</b> method does not guarantee exact seeking. The accuracy of the seek depends on the media content. If the media content contains a video stream, the <b>SetCurrentPosition</b> method typically seeks to the nearest key frame before the desired position. The distance between key frames depends on several factors, including the encoder implementation, the video content, and the particular encoding settings used to encode the content. The distance between key frame can vary within a single video file (for example, depending on scene complexity).

After seeking, the application should call <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a> and advance to the desired position. 

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

