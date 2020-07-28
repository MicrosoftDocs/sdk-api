---
UID: NF:wmsdkidl.IWMWriterPushSink.EndSession
title: IWMWriterPushSink::EndSession (wmsdkidl.h)
description: The EndSession method ends the push distribution session. This method sends an end-of-stream message to the server, and then shuts down the data path on the server.
helpviewer_keywords: ["EndSession","EndSession method [windows Media Format]","EndSession method [windows Media Format]","IWMWriterPushSink interface","IWMWriterPushSink interface [windows Media Format]","EndSession method","IWMWriterPushSink.EndSession","IWMWriterPushSink::EndSession","IWMWriterPushSinkEndSession","wmformat.iwmwriterpushsink_endsession","wmsdkidl/IWMWriterPushSink::EndSession"]
old-location: wmformat\iwmwriterpushsink_endsession.htm
tech.root: wmformat
ms.assetid: c2fa77a6-e159-4b10-b1ba-fbf96c7e09d4
ms.date: 12/05/2018
ms.keywords: EndSession, EndSession method [windows Media Format], EndSession method [windows Media Format],IWMWriterPushSink interface, IWMWriterPushSink interface [windows Media Format],EndSession method, IWMWriterPushSink.EndSession, IWMWriterPushSink::EndSession, IWMWriterPushSinkEndSession, wmformat.iwmwriterpushsink_endsession, wmsdkidl/IWMWriterPushSink::EndSession
f1_keywords:
- wmsdkidl/IWMWriterPushSink.EndSession
dev_langs:
- c++
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmvcore.lib
- Wmvcore.dll
- WMStubDRM.lib
- WMStubDRM.dll
api_name:
- IWMWriterPushSink.EndSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterPushSink::EndSession


## -description



The <b>EndSession</b> method ends the push distribution session. This method sends an end-of-stream message to the server, and then shuts down the data path on the server.




## -parameters






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
<dt><b>NS_E_CONNECTION_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A connection failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
There is no connection to the server. (Possibly this method was called before any connection was made.)

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink">IWMWriterPushSink Interface</a>
 

 

