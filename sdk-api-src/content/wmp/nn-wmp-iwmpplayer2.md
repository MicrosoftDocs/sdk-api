---
UID: NN:wmp.IWMPPlayer2
title: IWMPPlayer2 (wmp.h)
description: The IWMPPlayer2 interface provides additional methods for modifying the basic behavior of the Windows Media Player control user interface.
helpviewer_keywords: ["IWMPPlayer2","IWMPPlayer2 interface [Windows Media Player]","IWMPPlayer2 interface [Windows Media Player]","described","IWMPPlayer2Interface","wmp.iwmpplayer2","wmp/IWMPPlayer2"]
old-location: wmp\iwmpplayer2.htm
tech.root: WMP
ms.assetid: bf51d54d-d0aa-42ad-8180-d1f6487baac8
ms.date: 12/05/2018
ms.keywords: IWMPPlayer2, IWMPPlayer2 interface [Windows Media Player], IWMPPlayer2 interface [Windows Media Player],described, IWMPPlayer2Interface, wmp.iwmpplayer2, wmp/IWMPPlayer2
f1_keywords:
- wmp/IWMPPlayer2
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
- IWMPPlayer2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPPlayer2 interface


## -description



The <b>IWMPPlayer2</b> interface provides additional methods for modifying the basic behavior of the Windows Media Player control user interface. These methods also supplement the <b>IWMPCore</b> interface.

The <b>IWMPPlayer2</b> interface duplicates the methods of <b>IWMPPlayer</b>, inherits the methods of <b>IWMPCore</b>, and exposes the following additional methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPPlayer2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPPlayer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPPlayer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-get_stretchtofit">get_stretchToFit</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether video will stretch to fit size of the Windows Media Player control video display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-get_windowlessvideo">get_windowlessVideo</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-put_stretchtofit">put_stretchToFit</a>
</td>
<td align="left" width="63%">
Specifies whether video will stretch to fit the size of the Windows Media Player control video display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpplayer2-put_windowlessvideo">put_windowlessVideo</a>
</td>
<td align="left" width="63%">
Specifies whether the Windows Media Player control renders video in windowless mode.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPPlayer2</b> interface either by calling the <b>QueryInterface</b> method of the <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer</a> interface or by calling the COM <b>CoCreateInstance</b> method.

	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer3">IWMPPlayer3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

