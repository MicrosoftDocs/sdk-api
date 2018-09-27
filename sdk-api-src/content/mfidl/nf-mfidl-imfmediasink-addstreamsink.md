---
UID: NF:mfidl.IMFMediaSink.AddStreamSink
title: IMFMediaSink::AddStreamSink
author: windows-sdk-content
description: Adds a new stream sink to the media sink.
old-location: mf\imfmediasink_addstreamsink.htm
tech.root: medfound
ms.assetid: 1b05ef87-5559-4310-942c-54ab113eb42d
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: 1b05ef87-5559-4310-942c-54ab113eb42d, AddStreamSink, AddStreamSink method [Media Foundation], AddStreamSink method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],AddStreamSink method, IMFMediaSink.AddStreamSink, IMFMediaSink::AddStreamSink, mf.imfmediasink_addstreamsink, mfidl/IMFMediaSink::AddStreamSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSink.AddStreamSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSink::AddStreamSink


## -description



Adds a new stream sink to the media sink.




## -parameters




### -param dwStreamSinkIdentifier [in]

Identifier for the new stream. The value is arbitrary but must be unique.


### -param pMediaType [in]

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface, specifying the media type for the stream. This parameter can be <b>NULL</b>.


### -param ppStreamSink [out]

Receives a pointer to the new stream sink's <a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a> interface. The caller must release the interface.


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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The specified stream identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">Shutdown</a> method has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
There is already a stream sink with the same stream identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINKS_FIXED</b></dt>
</dl>
</td>
<td width="60%">
This media sink has a fixed set of stream sinks. New stream sinks cannot be added.

</td>
</tr>
</table>
 




## -remarks



Not all media sinks support this method. If the media sink does not support this method, the <a href="https://msdn.microsoft.com/a7e8e2af-8b10-47f5-8b09-a7147ace5ba1">IMFMediaSink::GetCharacteristics</a> method returns the MEDIASINK_FIXED_STREAMS flag.

If <i>pMediaType</i> is <b>NULL</b>, use the <a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a> interface to set the media type. Call <a href="https://msdn.microsoft.com/819d06b1-6b52-4496-bed8-a08b8f0b6153">IMFStreamSink::GetMediaTypeHandler</a> to get a pointer to the interface.




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

