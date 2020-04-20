---
UID: NN:wmp.IWMPEvents4
title: IWMPEvents4 (wmp.h)
description: The IWMPEvents4 interface provides access to an event originating from the Windows Media Player 12 control so that an application that has this control embedded in it can respond to the event.helpviewer_keywords: ["IWMPEvents4","IWMPEvents4 interface [Windows Media Player]","IWMPEvents4 interface [Windows Media Player]","described","wmp.iwmpevents4","wmp/IWMPEvents4"]
old-location: wmp\iwmpevents4.htm
tech.root: WMP
ms.assetid: b846ef23-1206-4a0b-866f-558b99b73f1d
ms.date: 12/05/2018
ms.keywords: IWMPEvents4, IWMPEvents4 interface [Windows Media Player], IWMPEvents4 interface [Windows Media Player],described, wmp.iwmpevents4, wmp/IWMPEvents4
f1_keywords:
- wmp/IWMPEvents4
dev_langs:
- c++
req.header: wmp.h
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
- wmp.h
api_name:
- IWMPEvents4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents4 interface


## -description


The <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents4</a> interface provides access to an event originating from the Windows Media Player 12 control so that an application that has this control embedded in it can respond to the event. The event exposed by <b>IWMPEvents4</b> is also exposed by the <a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPEvents4</b> interface inherits from <b>IWMPEvents3</b>. <b>IWMPEvents4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPEvents4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/WMP/iwmpevents4-syncestimationcomplete">SyncEstimationComplete</a>
</td>
<td align="left" width="63%">
Occurs when a size estimation, previously initiated by <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize">IWMPSyncDevice3::estimateSyncSize</a>, is complete.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/handling-events-in-c">Handling Events in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
 

 

