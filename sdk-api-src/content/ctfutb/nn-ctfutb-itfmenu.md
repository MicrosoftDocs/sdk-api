---
UID: NN:ctfutb.ITfMenu
title: ITfMenu (ctfutb.h)
description: The ITfMenu interface is implemented by the language bar and used by a language bar button provider to add items to the menu that the language bar will display for the button.
helpviewer_keywords: ["ITfMenu","ITfMenu interface [Text Services Framework]","ITfMenu interface [Text Services Framework]","described","_tsf_itfmenu_ref","ctfutb/ITfMenu","tsf.itfmenu"]
old-location: tsf\itfmenu.htm
tech.root: TSF
ms.assetid: 303115e1-8d52-4a0a-b05e-b5c92b8b3e2a
ms.date: 12/05/2018
ms.keywords: ITfMenu, ITfMenu interface [Text Services Framework], ITfMenu interface [Text Services Framework],described, _tsf_itfmenu_ref, ctfutb/ITfMenu, tsf.itfmenu
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfMenu
 - ctfutb/ITfMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfMenu
---

# ITfMenu interface


## -description

The <b>ITfMenu</b> interface is implemented by the language bar and used by a language bar button provider to add items to the menu that the language bar will display for the button.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfMenu</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfMenu</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfMenu</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itfmenu-addmenuitem">AddMenuItem</a>
</td>
<td align="left" width="63%">
Adds an item to the menu that the language bar will display for the button.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-initmenu">ITfLangBarItemBitmapButton::InitMenu
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-initmenu">ITfLangBarItemButton::InitMenu
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu">ITfSystemLangBarItemSink::InitMenu
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

