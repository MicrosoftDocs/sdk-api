---
UID: NN:ctfutb.ITfLangBarItem
title: ITfLangBarItem (ctfutb.h)
description: The ITfLangBarItem interface is implemented by a language bar item provider and used by the language bar manager to obtain detailed information about the language bar item.helpviewer_keywords: ["ITfLangBarItem","ITfLangBarItem interface [Text Services Framework]","ITfLangBarItem interface [Text Services Framework]","described","_tsf_itflangbaritem_ref","ctfutb/ITfLangBarItem","tsf.itflangbaritem"]
old-location: tsf\itflangbaritem.htm
tech.root: TSF
ms.assetid: 16612641-2bff-4e6f-a955-85793021a20b
ms.date: 12/05/2018
ms.keywords: ITfLangBarItem, ITfLangBarItem interface [Text Services Framework], ITfLangBarItem interface [Text Services Framework],described, _tsf_itflangbaritem_ref, ctfutb/ITfLangBarItem, tsf.itflangbaritem
f1_keywords:
- ctfutb/ITfLangBarItem
dev_langs:
- c++
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
- ITfLangBarItem
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarItem interface


## -description


The <b>ITfLangBarItem</b> interface is implemented by a language bar item provider and used by the language bar manager to obtain detailed information about the language bar item. An instance of this interface is provided to the language bar manager by the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Obtains information about the language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Obtains the status of a language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring">GetTooltipString</a>
</td>
<td align="left" width="63%">
Obtains the text to be displayed in the tooltip for the language bar item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-show">Show</a>
</td>
<td align="left" width="63%">
Called to show or hide the language bar item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

