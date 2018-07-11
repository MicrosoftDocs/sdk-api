---
UID: NN:wmsdkidl.IWMWriterPushSink
title: IWMWriterPushSink
author: windows-sdk-content
description: The IWMWriterPushSink interface enables the application to send ASF files to a publishing point on a Windows Media server.
old-location: wmformat\iwmwriterpushsink.htm
old-project: wmformat
ms.assetid: 47bee154-0d29-4f4c-ac38-af8747088024
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMWriterPushSink, IWMWriterPushSink interface [windows Media Format], IWMWriterPushSink interface [windows Media Format],described, IWMWriterPushSinkInterface, wmformat.iwmwriterpushsink, wmsdkidl/IWMWriterPushSink
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterPushSink interface


## -description



The <b>IWMWriterPushSink</b> interface enables the application to send ASF files to a publishing point on a Windows Media server. The writer push sink object exposes this interface. To create an instance of the writer push sink, call the <a href="https://msdn.microsoft.com/544aa6d4-a8fe-4ce5-b329-01b031aa3e6f">WMCreateWriterPushSink</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterPushSink</b> interface inherits from <a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>. <b>IWMWriterPushSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5934697e-5d7c-4681-a424-9ad764dfeab1">Connect</a>
</td>
<td align="left" width="63%">
Connects to a publishing point on a Windows Media server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37e8badb-139a-45bf-84bc-bb071d128847">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the push sink from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543004">EndSession</a>
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
<a href="https://msdn.microsoft.com/3831b727-7fdc-4d05-a7b3-86ca5b5c3b17">IWMRegisterCallback</a>
</td>
<td>IID_ 
IWMRegisterCallback</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>
</td>
<td>IID_IWMWriterSink</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/73656814-7fac-4567-abcd-dbb3243fcaa8">IWMWriterSink</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8f01beae-4270-4cf5-afff-3f7014cae90f">Sending ASF Data to a Publishing Point</a>



<a href="https://msdn.microsoft.com/34e48f35-13d7-4649-a8b2-ed6510b16f88">Writer Push Sink Object</a>
 

 

