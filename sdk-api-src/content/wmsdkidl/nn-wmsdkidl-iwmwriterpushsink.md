---
UID: NN:wmsdkidl.IWMWriterPushSink
title: IWMWriterPushSink (wmsdkidl.h)

description: The IWMWriterPushSink interface enables the application to send ASF files to a publishing point on a Windows Media server.
old-location: wmformat\iwmwriterpushsink.htm
tech.root: wmformat
ms.assetid: 47bee154-0d29-4f4c-ac38-af8747088024

ms.date: 12/05/2018
ms.keywords: IWMWriterPushSink, IWMWriterPushSink interface [windows Media Format], IWMWriterPushSink interface [windows Media Format],described, IWMWriterPushSinkInterface, wmformat.iwmwriterpushsink, wmsdkidl/IWMWriterPushSink
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMWriterPushSink"
dev_langs:
 - c++
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMWriterPushSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterPushSink interface


## -description



The <b>IWMWriterPushSink</b> interface enables the application to send ASF files to a publishing point on a Windows Media server. The writer push sink object exposes this interface. To create an instance of the writer push sink, call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink">WMCreateWriterPushSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPushSink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>. <b>IWMWriterPushSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterPushSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects to a publishing point on a Windows Media server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the push sink from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession">EndSession</a>
</td>
<td align="left" width="63%">
Ends the push distribution session.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.
<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback">IWMRegisterCallback</a>
</td>
<td>IID_ 
IWMRegisterCallback</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/sending-asf-data-to-a-publishing-point">Sending ASF Data to a Publishing Point</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-push-sink-object">Writer Push Sink Object</a>
 

 

