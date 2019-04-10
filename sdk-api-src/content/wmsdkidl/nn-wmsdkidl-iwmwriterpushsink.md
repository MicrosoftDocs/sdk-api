---
UID: NN:wmsdkidl.IWMWriterPushSink
title: IWMWriterPushSink (wmsdkidl.h)
author: windows-sdk-content
description: The IWMWriterPushSink interface enables the application to send ASF files to a publishing point on a Windows Media server.
old-location: wmformat\iwmwriterpushsink.htm
tech.root: wmformat
ms.assetid: 47bee154-0d29-4f4c-ac38-af8747088024
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMWriterPushSink, IWMWriterPushSink interface [windows Media Format], IWMWriterPushSink interface [windows Media Format],described, IWMWriterPushSinkInterface, wmformat.iwmwriterpushsink, wmsdkidl/IWMWriterPushSink
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterPushSink interface


## -description



The <b>IWMWriterPushSink</b> interface enables the application to send ASF files to a publishing point on a Windows Media server. The writer push sink object exposes this interface. To create an instance of the writer push sink, call the <a href="https://msdn.microsoft.com/en-us/library/Dd757792(v=VS.85).aspx">WMCreateWriterPushSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPushSink</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink</a>. <b>IWMWriterPushSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757464(v=VS.85).aspx">Connect</a>
</td>
<td align="left" width="63%">
Connects to a publishing point on a Windows Media server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757465(v=VS.85).aspx">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the push sink from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757466(v=VS.85).aspx">EndSession</a>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd743613(v=VS.85).aspx">IWMRegisterCallback</a>
</td>
<td>IID_ 
IWMRegisterCallback</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757467(v=VS.85).aspx">IWMWriterSink</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8f01beae-4270-4cf5-afff-3f7014cae90f">Sending ASF Data to a Publishing Point</a>



<a href="https://msdn.microsoft.com/34e48f35-13d7-4649-a8b2-ed6510b16f88">Writer Push Sink Object</a>
 

 

