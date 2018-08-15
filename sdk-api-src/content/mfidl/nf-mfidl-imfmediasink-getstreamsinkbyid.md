---
UID: NF:mfidl.IMFMediaSink.GetStreamSinkById
title: IMFMediaSink::GetStreamSinkById
author: windows-sdk-content
description: Gets a stream sink, specified by stream identifier.
old-location: mf\imfmediasink_getstreamsinkbyid.htm
old-project: medfound
ms.assetid: 267a8efc-6743-48ca-a1c4-da82f3770419
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 267a8efc-6743-48ca-a1c4-da82f3770419, GetStreamSinkById, GetStreamSinkById method [Media Foundation], GetStreamSinkById method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetStreamSinkById method, IMFMediaSink.GetStreamSinkById, IMFMediaSink::GetStreamSinkById, mf.imfmediasink_getstreamsinkbyid, mfidl/IMFMediaSink::GetStreamSinkById
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
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
 - IMFMediaSink.GetStreamSinkById
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSink::GetStreamSinkById


## -description



Gets a stream sink, specified by stream identifier.




## -parameters




### -param dwStreamSinkIdentifier [in]

Stream identifier of the stream sink.


### -param ppStreamSink [out]

Receives a pointer to the stream's <a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a> interface. The caller must release the interface.


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
The stream identifier is not valid.

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
</table>
 




## -remarks



If you add a stream sink by calling the <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">IMFMediaSink::AddStreamSink</a> method, the stream identifier is specified in the <i>dwStreamSinkIdentifier</i> parameter of that method. If the media sink has a fixed set of streams, the media sink assigns the stream identifiers.

To enumerate the streams by index number instead of stream identifier, call <a href="https://msdn.microsoft.com/01604801-1566-410c-b23a-0568c7298868">IMFMediaSink::GetStreamSinkByIndex</a>.




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

