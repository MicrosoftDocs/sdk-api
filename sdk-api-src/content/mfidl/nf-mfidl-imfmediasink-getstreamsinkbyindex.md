---
UID: NF:mfidl.IMFMediaSink.GetStreamSinkByIndex
title: IMFMediaSink::GetStreamSinkByIndex
author: windows-sdk-content
description: Gets a stream sink, specified by index.
old-location: mf\imfmediasink_getstreamsinkbyindex.htm
tech.root: medfound
ms.assetid: 01604801-1566-410c-b23a-0568c7298868
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 01604801-1566-410c-b23a-0568c7298868, GetStreamSinkByIndex, GetStreamSinkByIndex method [Media Foundation], GetStreamSinkByIndex method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetStreamSinkByIndex method, IMFMediaSink.GetStreamSinkByIndex, IMFMediaSink::GetStreamSinkByIndex, mf.imfmediasink_getstreamsinkbyindex, mfidl/IMFMediaSink::GetStreamSinkByIndex
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
 - IMFMediaSink.GetStreamSinkByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSink::GetStreamSinkByIndex


## -description



Gets a stream sink, specified by index.




## -parameters




### -param dwIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="https://msdn.microsoft.com/bf4b5713-586c-4b12-80a1-4452eec63e32">IMFMediaSink::GetStreamSinkCount</a>.


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
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid index.

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



Enumerating stream sinks is not a thread-safe operation, because stream sinks can be added or removed between calls to this method.




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

