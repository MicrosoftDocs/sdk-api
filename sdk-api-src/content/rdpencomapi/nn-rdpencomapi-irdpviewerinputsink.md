---
UID: NN:rdpencomapi.IRDPViewerInputSink
title: IRDPViewerInputSink
author: windows-sdk-content
description: Sends mouse and keyboard events, and supports touch input.
old-location: rdp\irdpviewerinputsink.htm
old-project: Rdp
ms.assetid: 364EC709-C41C-4ADD-8E7D-6A635E5BCCDA
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: IRDPViewerInputSink, IRDPViewerInputSink class [RDP], IRDPViewerInputSink class [RDP],described, rdp.irdpviewerinputsink, rdpencomapi/IRDPViewerInputSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPViewerInputSink
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRDPViewerInputSink interface


## -description


<p class="CCE_Message">[The <b>IRDPViewerInputSink</b> interface is no longer available for use for UWP applications as of Windows 10, version 1709. It is still supported for Desktop apps.]

Sends mouse and keyboard events, and supports touch input.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPViewerInputSink</b> class inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPViewerInputSink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5DD220B8-505E-43AE-9438-F1D553AABB0B">AddTouchInput</a>
</td>
<td align="left" width="63%">
Accepts a description of  a touch input.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DCB67D63-A866-4D98-907B-6CDB7EB56312">BeginTouchFrame</a>
</td>
<td align="left" width="63%">
Begins  to accept a series of touch inputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31E84AEB-7A89-4EF1-9744-3102AAEA2C1E">EndTouchFrame</a>
</td>
<td align="left" width="63%">
Stops  to   accept  a series of touch inputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28EDA0AD-9669-4232-BD41-4ADEC90CA3A7">SendKeyboardEvent</a>
</td>
<td align="left" width="63%">
Sends a keyboard event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2BC93D69-7DBC-4C38-9980-EEB9775A083E">SendMouseButtonEvent</a>
</td>
<td align="left" width="63%">
Sends a mouse button event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0888E762-A0B3-48EA-B928-42E3E801AF15">SendMouseMoveEvent</a>
</td>
<td align="left" width="63%">
Sends a mouse move event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CEC54C27-F49E-4B41-A18D-69F0414955A1">SendMouseWheelEvent</a>
</td>
<td align="left" width="63%">
Sends a mouse wheel event message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8B59CAF-DFBE-4569-99B2-DECF1F1DBB56">SendSyncEvent</a>
</td>
<td align="left" width="63%">
Sends an event message to indicate a change in the state of the keyboard, such as when the Caps Lock key is pressed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bb1df622-bfcd-4d84-b5f6-780b693cc760">Windows Desktop Sharing Interfaces</a>
 

 

