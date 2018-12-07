---
UID: NN:msctf.ITfMouseSink
title: ITfMouseSink
author: windows-sdk-content
description: The ITfMouseSink interface is implemented by a text service to receive mouse event notifications. A mouse event sink is installed with the ITfMouseTracker::AdviseMouseSink method of one of the ITfMouseTracker interfaces.
old-location: tsf\itfmousesink.htm
tech.root: TSF
ms.assetid: d6e5549e-768d-47af-a553-84430641cda4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfMouseSink, ITfMouseSink interface [Text Services Framework], ITfMouseSink interface [Text Services Framework],described, _tsf_itfmousesink_ref, msctf/ITfMouseSink, tsf.itfmousesink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfMouseSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfMouseSink interface


## -description


The <b>ITfMouseSink</b> interface is implemented by a text service to receive mouse event notifications. A mouse event sink is installed with the <a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink</a> method of one of the <a href="https://msdn.microsoft.com/aad07b35-99e0-4c76-ba65-93c2c972303d">ITfMouseTracker</a> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMouseSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfMouseSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMouseSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1aa4fdb7-b16d-4e58-934a-8323450f6749">OnMouseEvent</a>
</td>
<td align="left" width="63%">
Called when a mouse event occurs over a range of text.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink
      </a>



<a href="https://msdn.microsoft.com/365538cd-0f18-45ce-91c2-ee3255b7fa93">ITfMouseTrackerACP::AdviseMouseSink
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

