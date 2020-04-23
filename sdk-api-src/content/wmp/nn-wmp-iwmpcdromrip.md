---
UID: NN:wmp.IWMPCdromRip
title: IWMPCdromRip (wmp.h)
description: The IWMPCdromRip interface provides methods to manage copying, or ripping, tracks from an audio CD.Ripping a CD by using the IWMPCdromRip interface has the same effect as ripping music by using the Windows Media Player user interface.helpviewer_keywords: ["IWMPCdromRip","IWMPCdromRip interface [Windows Media Player]","IWMPCdromRip interface [Windows Media Player]","described","IWMPCdromRipInterface","wmp.iwmpcdromrip","wmp/IWMPCdromRip"]
old-location: wmp\iwmpcdromrip.htm
tech.root: WMP
ms.assetid: c3e2db46-bef0-4c79-91b5-97ca5a86c6ba
ms.date: 12/05/2018
ms.keywords: IWMPCdromRip, IWMPCdromRip interface [Windows Media Player], IWMPCdromRip interface [Windows Media Player],described, IWMPCdromRipInterface, wmp.iwmpcdromrip, wmp/IWMPCdromRip
f1_keywords:
- wmp/IWMPCdromRip
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
- IWMPCdromRip
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCdromRip interface


## -description



The <b>IWMPCdromRip</b> interface provides methods to manage copying, or <i>ripping</i>, tracks from an audio CD.

Ripping a CD by using the <b>IWMPCdromRip</b> interface has the same effect as ripping music by using the Windows Media Player user interface. Ripped content is automatically added to the library according to the user's preferences. For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCdromRip</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPCdromRip</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPCdromRip</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress">get_ripProgress</a>
</td>
<td align="left" width="63%">
Retrieves the CD ripping progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate">get_ripState</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration value that indicates the current state of the ripping process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip">startRip</a>
</td>
<td align="left" width="63%">
Rips the CD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip">stopRip</a>
</td>
<td align="left" width="63%">
Stops the CD ripping process.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/ripping-a-cd">Ripping a CD</a>
 

 

