---
UID: NN:rdpencomapi.IRDPSRAPIClipboardUseEvents
title: IRDPSRAPIClipboardUseEvents (rdpencomapi.h)
author: windows-sdk-content
description: Implement this interface on the sharer side to track or control use of the clipboard. If you do not enable clipboard sharing, this interface has no effect. You need to set a value for the SetClipboardRedirectCallback property described in Property.
old-location: rdp\irdpsrapiclipboarduseevents.htm
tech.root: rdp
ms.assetid: 76ea520c-64c2-4096-ab21-9714b98b5dac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIClipboardUseEvents, IRDPSRAPIClipboardUseEvents interface [RDP], IRDPSRAPIClipboardUseEvents interface [RDP],described, rdp.irdpsrapiclipboarduseevents, rdpencomapi/IRDPSRAPIClipboardUseEvents
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
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
 - RdpEncomAPI.h
api_name:
 - IRDPSRAPIClipboardUseEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPIClipboardUseEvents interface


## -description


Implement this interface on the sharer side to track or control use of the clipboard. 
If you do not enable clipboard sharing, this interface has no effect. You need to set a value for the <b>SetClipboardRedirectCallback</b> property described in <a href="https://msdn.microsoft.com/01aee262-95c0-4065-8f8c-e21db66f2a8c">Property</a>.

This interface is available starting with Windows 10, version 1511.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIClipboardUseEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPSRAPIClipboardUseEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPSRAPIClipboardUseEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa5fccb9-ca7b-4779-a454-f16be8bca72c">OnPasteFromClipboard</a>
</td>
<td align="left" width="63%">
This callback is issued when an attempt to copy data from the sharer computer is made.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/01aee262-95c0-4065-8f8c-e21db66f2a8c">Property</a>
 

 

