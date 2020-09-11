---
UID: NN:wmpservices.IWMPTranscodePolicy
title: IWMPTranscodePolicy (wmpservices.h)
description: The IWMPTranscodePolicy interface provides a method implemented by DirectShow source filters to manage changing the format of digital media files.
helpviewer_keywords: ["IWMPTranscodePolicy","IWMPTranscodePolicy interface [Windows Media Player]","IWMPTranscodePolicy interface [Windows Media Player]","described","IWMPTranscodePolicyInterface","wmp.iwmptranscodepolicy","wmpservices/IWMPTranscodePolicy"]
old-location: wmp\iwmptranscodepolicy.htm
tech.root: WMP
ms.assetid: b7dbd25f-6865-44fa-9d46-e77de393ce13
ms.date: 12/05/2018
ms.keywords: IWMPTranscodePolicy, IWMPTranscodePolicy interface [Windows Media Player], IWMPTranscodePolicy interface [Windows Media Player],described, IWMPTranscodePolicyInterface, wmp.iwmptranscodepolicy, wmpservices/IWMPTranscodePolicy
req.header: wmpservices.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPTranscodePolicy
 - wmpservices/IWMPTranscodePolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPTranscodePolicy
---

# IWMPTranscodePolicy interface


## -description

The <b>IWMPTranscodePolicy</b> interface provides a method implemented by DirectShow source filters to manage changing the format of digital media files.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPTranscodePolicy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPTranscodePolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPTranscodePolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode">allowTranscode</a>
</td>
<td align="left" width="63%">
Retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to Windows Media Format.

</td>
</tr>
</table> 

To retrieve a pointer to the <b>IWMPTranscodePolicy</b> interface, Windows Media Player calls the <b>QueryInterface</b> method of the DirectShow source filter.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>

