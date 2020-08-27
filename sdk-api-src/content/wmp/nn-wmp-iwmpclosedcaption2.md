---
UID: NN:wmp.IWMPClosedCaption2
title: IWMPClosedCaption2 (wmp.h)
description: The IWMPClosedCaption2 interface provides closed captioning methods that supplement the IWMPClosedCaption interface.
helpviewer_keywords: ["IWMPClosedCaption2","IWMPClosedCaption2 interface [Windows Media Player]","IWMPClosedCaption2 interface [Windows Media Player]","described","IWMPClosedCaption2Interface","wmp.iwmpclosedcaption2","wmp/IWMPClosedCaption2"]
old-location: wmp\iwmpclosedcaption2.htm
tech.root: WMP
ms.assetid: 21067ac1-d29e-4f1b-b123-34b24929369a
ms.date: 12/05/2018
ms.keywords: IWMPClosedCaption2, IWMPClosedCaption2 interface [Windows Media Player], IWMPClosedCaption2 interface [Windows Media Player],described, IWMPClosedCaption2Interface, wmp.iwmpclosedcaption2, wmp/IWMPClosedCaption2
f1_keywords:
- wmp/IWMPClosedCaption2
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
- IWMPClosedCaption2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPClosedCaption2 interface


## -description



The <b>IWMPClosedCaption2</b> interface provides closed captioning methods that supplement the <b>IWMPClosedCaption</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPClosedCaption2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption</a>. <b>IWMPClosedCaption2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPClosedCaption2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption2-get_samilangcount">get_SAMILangCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of languages supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption2-get_samistylecount">get_SAMIStyleCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of styles supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption2-getsamilangid">getSAMILangID</a>
</td>
<td align="left" width="63%">
Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption2-getsamilangname">getSAMILangName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a language supported by the current SAMI file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpclosedcaption2-getsamistylename">getSAMIStyleName</a>
</td>
<td align="left" width="63%">
Retrieves the name of a style supported by the current SAMI file.

</td>
</tr>
</table> 

Retrieve a pointer to an <b>IWMPClosedCaption2</b> interface by calling the <b>QueryInterface</b> method of the <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption</a> interface.

	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/adding-closed-captions-to-digital-media">Adding Closed Captions to Digital Media</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

