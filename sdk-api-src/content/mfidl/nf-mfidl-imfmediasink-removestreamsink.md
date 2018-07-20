---
UID: NF:mfidl.IMFMediaSink.RemoveStreamSink
title: IMFMediaSink::RemoveStreamSink
author: windows-sdk-content
description: Removes a stream sink from the media sink.
old-location: mf\imfmediasink_removestreamsink.htm
old-project: medfound
ms.assetid: f99ee960-7fea-4867-bc24-d7e1d6fcafa5
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFMediaSink interface [Media Foundation],RemoveStreamSink method, IMFMediaSink.RemoveStreamSink, IMFMediaSink::RemoveStreamSink, RemoveStreamSink, RemoveStreamSink method [Media Foundation], RemoveStreamSink method [Media Foundation],IMFMediaSink interface, f99ee960-7fea-4867-bc24-d7e1d6fcafa5, mf.imfmediasink_removestreamsink, mfidl/IMFMediaSink::RemoveStreamSink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSink.RemoveStreamSink
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSink::RemoveStreamSink


## -description



Removes a stream sink from the media sink.




## -parameters




### -param dwStreamSinkIdentifier [in]

Identifier of the stream to remove. The stream identifier is defined when you call <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">IMFMediaSink::AddStreamSink</a> to add the stream sink.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
This particular stream sink cannot be removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream number is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The media sink has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINKS_FIXED</b></dt>
</dl>
</td>
<td width="60%">
This media sink has a fixed set of stream sinks. Stream sinks cannot be removed.

</td>
</tr>
</table>
 




## -remarks



After this method is called, the corresponding stream sink object is no longer valid. The <a href="https://msdn.microsoft.com/01604801-1566-410c-b23a-0568c7298868">IMFMediaSink::GetStreamSinkByIndex</a> and <a href="https://msdn.microsoft.com/267a8efc-6743-48ca-a1c4-da82f3770419">IMFMediaSink::GetStreamSinkById</a> methods will no longer return that stream sink. You can re-use the stream identifier if you add another stream (by calling <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">AddStreamSink</a>).

Not all media sinks support this method. If the media sink does not support this method, the <a href="https://msdn.microsoft.com/a7e8e2af-8b10-47f5-8b09-a7147ace5ba1">IMFMediaSink::GetCharacteristics</a> method returns the MEDIASINK_FIXED_STREAMS flag.

In some cases, the media sink supports this method but does not allow every stream sink to be removed. (For example, it might not allow stream 0 to be removed.)




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

