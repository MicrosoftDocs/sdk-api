---
UID: NF:mfidl.IMFStreamSink.GetIdentifier
title: IMFStreamSink::GetIdentifier (mfidl.h)
author: windows-sdk-content
description: Retrieves the stream identifier for this stream sink.
old-location: mf\imfstreamsink_getidentifier.htm
tech.root: medfound
ms.assetid: af4855f6-36fa-4949-8b93-9e630a12e71b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIdentifier, GetIdentifier method [Media Foundation], GetIdentifier method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],GetIdentifier method, IMFStreamSink.GetIdentifier, IMFStreamSink::GetIdentifier, af4855f6-36fa-4949-8b93-9e630a12e71b, mf.imfstreamsink_getidentifier, mfidl/IMFStreamSink::GetIdentifier
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
 - IMFStreamSink.GetIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFStreamSink::GetIdentifier


## -description



Retrieves the stream identifier for this stream sink.




## -parameters




### -param pdwIdentifier [out]

Receives the stream identifier. If this stream sink was added by calling <a href="https://msdn.microsoft.com/1b05ef87-5559-4310-942c-54ab113eb42d">IMFMediaSink::AddStreamSink</a>, the stream identifier is in the <i>dwStreamSinkIdentifier</i> parameter of that method. Otherwise, the media sink defines the identifier.


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
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

