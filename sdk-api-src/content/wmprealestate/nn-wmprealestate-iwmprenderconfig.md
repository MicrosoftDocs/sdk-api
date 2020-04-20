---
UID: NN:wmprealestate.IWMPRenderConfig
title: IWMPRenderConfig (wmprealestate.h)
description: The IWMPRenderConfig interface provides methods to specify or retrieve a value indicating whether Media Foundation&#8211;based playback is restricted to the current process.Note  Using this interface with protected content is not supported. .helpviewer_keywords: ["IWMPRenderConfig","IWMPRenderConfig interface [Windows Media Player]","IWMPRenderConfig interface [Windows Media Player]","described","IWMPRenderConfigInterface","wmp.iwmprenderconfig","wmprealestate/IWMPRenderConfig"]
old-location: wmp\iwmprenderconfig.htm
tech.root: WMP
ms.assetid: 01a4c79e-9867-47c0-9aca-b2f1596f1c2a
ms.date: 12/05/2018
ms.keywords: IWMPRenderConfig, IWMPRenderConfig interface [Windows Media Player], IWMPRenderConfig interface [Windows Media Player],described, IWMPRenderConfigInterface, wmp.iwmprenderconfig, wmprealestate/IWMPRenderConfig
f1_keywords:
- wmprealestate/IWMPRenderConfig
dev_langs:
- c++
req.header: wmprealestate.h
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
- wmprealestate.h
api_name:
- IWMPRenderConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPRenderConfig interface


## -description



The <b>IWMPRenderConfig</b> interface provides methods to specify or retrieve a value indicating whether Media Foundation–based playback is restricted to the current process.

<div class="alert"><b>Note</b>  Using this interface with protected content is not supported.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPRenderConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPRenderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPRenderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmprealestate/nf-wmprealestate-iwmprenderconfig-get_inproconly">get_inProcOnly</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether playback is restricted to the current process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmprealestate/nf-wmprealestate-iwmprenderconfig-put_inproconly">put_inProcOnly</a>
</td>
<td align="left" width="63%">
Specifies a value indicating whether playback is restricted to the current process.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPRenderConfig</b> by calling <b>QueryInterface</b> through a pointer to <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer</a>.

	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

