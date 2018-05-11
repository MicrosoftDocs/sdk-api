---
UID: NF:mfidl.IMFMediaSink.GetStreamSinkCount
title: IMFMediaSink::GetStreamSinkCount
author: windows-driver-content
description: Gets the number of stream sinks on this media sink.
old-location: mf\imfmediasink_getstreamsinkcount.htm
old-project: medfound
ms.assetid: bf4b5713-586c-4b12-80a1-4452eec63e32
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetStreamSinkCount, GetStreamSinkCount method [Media Foundation], GetStreamSinkCount method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetStreamSinkCount method, IMFMediaSink.GetStreamSinkCount, IMFMediaSink::GetStreamSinkCount, bf4b5713-586c-4b12-80a1-4452eec63e32, mf.imfmediasink_getstreamsinkcount, mfidl/IMFMediaSink::GetStreamSinkCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaSink.GetStreamSinkCount
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSink::GetStreamSinkCount


## -description



Gets the number of stream sinks on this media sink.




## -parameters




### -param pcStreamSinkCount [out]

Receives the number of stream sinks.


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
The media sink's <a href="https://msdn.microsoft.com/library/windows/hardware/dn926950">Shutdown</a> method has been called.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/a0fbce1b-0a16-4449-9eca-906fd9056a1c">Media Sinks</a>
 

 

