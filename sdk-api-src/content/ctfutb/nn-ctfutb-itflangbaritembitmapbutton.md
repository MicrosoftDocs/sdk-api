---
UID: NN:ctfutb.ITfLangBarItemBitmapButton
title: ITfLangBarItemBitmapButton (ctfutb.h)
description: The ITfLangBarItemBitmapButton interface is implemented by a language bar bitmap button provider and is used by the language bar manager to obtain information specific to a bitmap button item on the language bar.
helpviewer_keywords: ["ITfLangBarItemBitmapButton","ITfLangBarItemBitmapButton interface [Text Services Framework]","ITfLangBarItemBitmapButton interface [Text Services Framework]","described","_tsf_itflangbaritembitmapbutton_ref","ctfutb/ITfLangBarItemBitmapButton","tsf.itflangbaritembitmapbutton"]
old-location: tsf\itflangbaritembitmapbutton.htm
tech.root: TSF
ms.assetid: 29fcc913-fcc7-4321-918b-2c354dd751ff
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemBitmapButton, ITfLangBarItemBitmapButton interface [Text Services Framework], ITfLangBarItemBitmapButton interface [Text Services Framework],described, _tsf_itflangbaritembitmapbutton_ref, ctfutb/ITfLangBarItemBitmapButton, tsf.itflangbaritembitmapbutton
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
 - ITfLangBarItemBitmapButton
 - ctfutb/ITfLangBarItemBitmapButton
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
 - ITfLangBarItemBitmapButton
---

# ITfLangBarItemBitmapButton interface


## -description

The <b>ITfLangBarItemBitmapButton</b> interface is implemented by a language bar bitmap button provider and is used by the language bar manager to obtain information specific to a bitmap button item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> passed to <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a> with IID_ITfLangBarItemBitmapButton.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemBitmapButton</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemBitmapButton</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItemBitmapButton</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap">DrawBitmap</a>
</td>
<td align="left" width="63%">
Obtains the bitmap and mask for the bitmap button item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-getpreferredsize">GetPreferredSize</a>
</td>
<td align="left" width="63%">
Obtains the preferred size, in pixels, of the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext">GetText</a>
</td>
<td align="left" width="63%">
Obtains the text to be displayed for the bitmap button in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-initmenu">InitMenu</a>
</td>
<td align="left" width="63%">
Called to enable a language bar bitmap button, that has the TF_LBI_STYLE_BTN_MENU style, to add items to the menu that the language bar will display for the button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-onclick">OnClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks a language bar bitmap button that has the TF_LBI_STYLE_BTN_BUTTON or TF_LBI_STYLE_BTN_TOGGLE style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembitmapbutton-onmenuselect">OnMenuSelect</a>
</td>
<td align="left" width="63%">
Called when the user selects an item in the menu that the language bar displays for the button.

</td>
</tr>
</table>

## -remarks

A language bar bitmap button functions as a button item on the language bar that displays text and a small bitmap. The bitmap displayed for the item should not be larger than the size of a small icon. Obtain these dimensions by calling <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a> with SM_CXSMICON for the width and SM_CYSMICON for the height.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

