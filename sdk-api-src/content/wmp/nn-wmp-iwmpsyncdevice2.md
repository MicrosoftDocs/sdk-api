---
UID: NN:wmp.IWMPSyncDevice2
title: IWMPSyncDevice2 (wmp.h)
description: The IWMPSyncDevice2 interface provides a method that supplements the IWMPSyncDevice interface.To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.
old-location: wmp\iwmpsyncdevice2.htm
tech.root: WMP
ms.assetid: b47fc5ea-741d-4e47-baad-afeb659f1079
ms.date: 12/05/2018
ms.keywords: IWMPSyncDevice2, IWMPSyncDevice2 interface [Windows Media Player], IWMPSyncDevice2 interface [Windows Media Player],described, IWMPSyncDevice2Interface, wmp.iwmpsyncdevice2, wmp/IWMPSyncDevice2
f1_keywords:
- wmp/IWMPSyncDevice2
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
- IWMPSyncDevice2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSyncDevice2 interface


## -description



The <b>IWMPSyncDevice2</b> interface provides a method that supplements the <b>IWMPSyncDevice</b> interface.

To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPSyncDevice2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice</a>. <b>IWMPSyncDevice2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPSyncDevice2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo">setItemInfo</a>
</td>
<td align="left" width="63%">
Specifies an attribute value for a device.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPSyncDevice2</b> by calling <b>QueryInterface</b> through a pointer to <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice</a>.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice">IWMPSyncDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
 

 

