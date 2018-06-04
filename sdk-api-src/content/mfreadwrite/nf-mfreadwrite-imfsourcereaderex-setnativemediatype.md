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

# IMFSourceReaderEx::SetNativeMediaType


## -description


Sets the native media type for a stream on the media source.


## -parameters




### -param dwStreamIndex [in]


### -param pMediaType [in]

A pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface of the media type.


### -param pdwStreamFlags [out]

Receives a bitwise <b>OR</b> of zero or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READERF_ALLEFFECTSREMOVED"></a><a id="mf_source_readerf_alleffectsremoved"></a><dl>
<dt><b>MF_SOURCE_READERF_ALLEFFECTSREMOVED</b></dt>
</dl>
</td>
<td width="60%">
All effects were removed from the stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED"></a><a id="mf_source_readerf_currentmediatypechanged"></a><dl>
<dt><b>MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED</b></dt>
</dl>
</td>
<td width="60%">
The current output type changed.

</td>
</tr>
</table>
 


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_INVALIDSTREAMNUMBER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>dwStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



This method sets the output type that is produced by the media source. Unlike the <a href="https://msdn.microsoft.com/54caec4d-1393-487b-94ee-78563b2b4645">IMFSourceReader::SetCurrentMediaType</a> method, this method does not insert any decoders, video processors, or other transforms. The media source must support the specified media type natively. To get a list of supported types from the media source, call <a href="https://msdn.microsoft.com/4b514f8d-082f-4e84-b512-d4a59706a6d8">IMFSourceReader::GetNativeMediaType</a>.

In asynchronous mode, this method fails if a sample request is pending. In that case, wait for the <a href="https://msdn.microsoft.com/1f334b49-d297-478d-a037-2fc53a75ed52">OnReadSample</a> callback to be invoked before calling the method. For more information about using the Source Reader in asynchronous mode, see <a href="https://msdn.microsoft.com/99bd9bd7-d8d1-433a-bc5a-4b9761de5048">IMFSourceReader::ReadSample</a>.

This method can trigger a change in the output format for the stream. If so, the <b>MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED</b> flag is returned in the  <i>pdwStreamFlags</i> parameter. The method might also cause the Source Reader to remove any effects that were added by the <a href="https://msdn.microsoft.com/493BB3CF-044D-4E83-9FF7-BD2039358501">IMFSourceReaderEx::AddTransformForStream</a> method. If this occurs, the  <b>MF_SOURCE_READERF_ALLEFFECTSREMOVED</b> flag is returned in <i>pdwStreamFlags</i>. 

This method is useful with audio and video capture devices, because a device might support several output formats. This method enables the application to choose the device format before decoders and other transforms are added.




## -see-also




<a href="https://msdn.microsoft.com/59888F9B-C464-4045-AA77-03EE16E2B598">IMFSourceReaderEx</a>
 

 

