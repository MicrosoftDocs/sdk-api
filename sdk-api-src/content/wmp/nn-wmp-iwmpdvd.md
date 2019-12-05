---
UID: NN:wmp.IWMPDVD
title: IWMPDVD (wmp.h)
description: The IWMPDVD interface provides methods for working with DVDs.
old-location: wmp\iwmpdvd.htm
tech.root: WMP
ms.assetid: d133f1e1-cbeb-403d-b247-9f495cb6f0f7
ms.date: 12/05/2018
ms.keywords: IWMPDVD, IWMPDVD interface [Windows Media Player], IWMPDVD interface [Windows Media Player],described, IWMPDVDInterface, wmp.iwmpdvd, wmp/IWMPDVD
ms.topic: interface
f1_keywords:
- wmp/IWMPDVD
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
- IWMPDVD
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPDVD interface


## -description



The <b>IWMPDVD</b> interface provides methods for working with DVDs.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPDVD</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPDVD</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPDVD</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpdvd-back">back</a>
</td>
<td align="left" width="63%">
Changes the display from a submenu to its parent menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpdvd-get_domain">get_domain</a>
</td>
<td align="left" width="63%">
Retrieves the current domain of the DVD.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpdvd-get_isavailable">get_isAvailable</a>
</td>
<td align="left" width="63%">
Determines whether a specified type of information is available or a given action can be performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpdvd-resume">resume</a>
</td>
<td align="left" width="63%">
Changes to playback mode from menu mode, resuming at the same position as when the menu was invoked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpdvd-titlemenu">titleMenu</a>
</td>
<td align="left" width="63%">
Stops playback and displays the title menu.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpdvd-topmenu">topMenu</a>
</td>
<td align="left" width="63%">
Stops playback and displays the root menu.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPDVD</b> interface with the following method.

<table>
<tr>
<th>Interface</th>
<th>Method</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2</a>
</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore2-get_dvd">get_dvd</a>
</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

