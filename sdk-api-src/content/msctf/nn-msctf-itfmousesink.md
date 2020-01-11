---
UID: NN:msctf.ITfMouseSink
title: ITfMouseSink (msctf.h)
description: The ITfMouseSink interface is implemented by a text service to receive mouse event notifications. A mouse event sink is installed with the ITfMouseTracker::AdviseMouseSink method of one of the ITfMouseTracker interfaces.
old-location: tsf\itfmousesink.htm
tech.root: TSF
ms.assetid: d6e5549e-768d-47af-a553-84430641cda4
ms.date: 12/05/2018
ms.keywords: ITfMouseSink, ITfMouseSink interface [Text Services Framework], ITfMouseSink interface [Text Services Framework],described, _tsf_itfmousesink_ref, msctf/ITfMouseSink, tsf.itfmousesink
f1_keywords:
- msctf/ITfMouseSink
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfMouseSink interface


## -description


The <b>ITfMouseSink</b> interface is implemented by a text service to receive mouse event notifications. A mouse event sink is installed with the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">ITfMouseTracker::AdviseMouseSink</a> method of one of the <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfmousetracker">ITfMouseTracker</a> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMouseSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMouseSink</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfmousesink-onmouseevent">OnMouseEvent</a>
</td>
<td align="left" width="63%">
Called when a mouse event occurs over a range of text.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfmousetracker-advisemousesink">ITfMouseTracker::AdviseMouseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfmousetrackeracp-advisemousesink">ITfMouseTrackerACP::AdviseMouseSink
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

