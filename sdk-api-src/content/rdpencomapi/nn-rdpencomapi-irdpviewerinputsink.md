---
UID: NN:rdpencomapi.IRDPViewerInputSink
title: IRDPViewerInputSink (rdpencomapi.h)
author: windows-sdk-content
description: Sends mouse and keyboard events, and supports touch input.
old-location: rdp\irdpviewerinputsink.htm
tech.root: rdp
ms.assetid: 364EC709-C41C-4ADD-8E7D-6A635E5BCCDA
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPViewerInputSink, IRDPViewerInputSink class [RDP], IRDPViewerInputSink class [RDP],described, rdp.irdpviewerinputsink, rdpencomapi/IRDPViewerInputSink
ms.topic: interface
f1_keywords: ["rdpencomapi/IRDPViewerInputSink"]
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerInputSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPViewerInputSink interface


## -description


<p class="CCE_Message">[The <b>IRDPViewerInputSink</b> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends mouse and keyboard events, and supports touch input.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPViewerInputSink</b> class inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPViewerInputSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPViewerInputSink</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-addtouchinput">AddTouchInput</a>
</td>
<td align="left" width="63%">
Accepts a description of  a touch input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-begintouchframe">BeginTouchFrame</a>
</td>
<td align="left" width="63%">
Begins  to accept a series of touch inputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-endtouchframe">EndTouchFrame</a>
</td>
<td align="left" width="63%">
Stops  to   accept  a series of touch inputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-sendkeyboardevent">SendKeyboardEvent</a>
</td>
<td align="left" width="63%">
Sends a keyboard event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-sendmousebuttonevent">SendMouseButtonEvent</a>
</td>
<td align="left" width="63%">
Sends a mouse button event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-sendmousemoveevent">SendMouseMoveEvent</a>
</td>
<td align="left" width="63%">
Sends a mouse move event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-sendmousewheelevent">SendMouseWheelEvent</a>
</td>
<td align="left" width="63%">
Sends a mouse wheel event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerinputsink-sendsyncevent">SendSyncEvent</a>
</td>
<td align="left" width="63%">
Sends an event message to indicate a change in the state of the keyboard, such as when the Caps Lock key is pressed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rdp/windows-desktop-sharing-interfaces">Windows Desktop Sharing Interfaces</a>
 

 

