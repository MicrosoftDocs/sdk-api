---
UID: NF:mfidl.MFCreateTranscodeTopology
title: MFCreateTranscodeTopology function
author: windows-driver-content
description: Creates a partial transcode topology.
old-location: mf\mfcreatetranscodetopology.htm
old-project: medfound
ms.assetid: ef3f19bf-1db9-459d-9617-d6cca9d6aba7
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: MFCreateTranscodeTopology, MFCreateTranscodeTopology function [Media Foundation], mf.mfcreatetranscodetopology, mfidl/MFCreateTranscodeTopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mf.dll
api_name:
-	MFCreateTranscodeTopology
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFCreateTranscodeTopology function


## -description


Creates a partial transcode topology.

The underlying topology builder creates a partial topology by connecting the required pipeline objects:
source, encoder, and sink. The encoder and the sink are configured according to the settings specified by the caller in the transcode profile. 

To create the transcode profile object, call the <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a> function and set the required attributes by calling the appropriate the <a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a> methods. 

The configured transcode profile is passed to the <b>MFCreateTranscodeTopology</b> function, which creates the transcode topology with the appropriate settings. The caller can then set this topology on the Media Session and start the session to begin the encoding process. When the Media Session ends, the transcoded file is generated.


## -parameters




### -param pSrc [in]

A pointer to a media source that encapsulates the source file to be transcoded. The media source object exposes the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface and can be created by using the source resolver. For more information, see <a href="https://msdn.microsoft.com/94e2a411-96b8-4506-8491-78f4f5f286ce">Using the Source Resolver</a>.


### -param pwszOutputFilePath [in]

A pointer to a null-terminated string that contains the name and path of the output file to be generated.


### -param pProfile [in]

A pointer to the transcode profile that contains the configuration settings for the audio stream, the video stream, and the container to which the file is written. The transcode profile object exposes the <a href="https://msdn.microsoft.com/82e012e0-84d8-4791-8b6f-bda58b498a90">IMFTranscodeProfile</a> interface and must be created by calling the <a href="https://msdn.microsoft.com/2a482c6f-6e20-419a-a7eb-085c41cc8186">MFCreateTranscodeProfile</a> function. After the object has been created the caller must provide the configuration settings by calling appropriate the <b>IMFTranscodeProfile</b> methods.


### -param ppTranscodeTopo [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the transcode topology object. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.



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
The function call succeeded, and <i>ppTranscodeTopo</i> receives a pointer to the transcode topology.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszOutputFilePath</i> contains invalid characters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_MEDIA_SOURCE_NO_STREAMS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
No streams are selected in the media source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_NO_CONTAINERTYPE</b></dt>
</dl>
</td>
<td width="60%">
The profile does not contain the <a href="https://msdn.microsoft.com/97fd968a-6843-4695-aece-02f9acd618fd">MF_TRANSCODE_CONTAINERTYPE</a> attribute.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_NO_MATCHING_ENCODER</b></dt>
</dl>
</td>
<td width="60%">
For one or more streams, cannot find an encoder that accepts the media type given in the profile.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSCODE_PROFILE_NO_MATCHING_STREAMS</b></dt>
</dl>
</td>
<td width="60%">
The profile does not specify a media type for any of the selected streams on the media source.

</td>
</tr>
</table>
 




## -remarks



For example code that uses this function, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/60873aa6-46ec-4a73-94b9-0d8ac602f850">Tutorial: Encoding an MP4 File</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2397ca78-edb5-4756-bd07-00529db28f76">Tutorial: Encoding a WMA File</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>



<a href="https://msdn.microsoft.com/24bf68a8-39bf-4302-b28c-71bb23b63469">Transcode API</a>
 

 

