---
UID: NN:ctfutb.ITfLangBarItemButton
title: ITfLangBarItemButton (ctfutb.h)
author: windows-sdk-content
description: The ITfLangBarItemButton interface is implemented by a language bar button provider and used by the language bar manager to obtain information about a button item on the language bar.
old-location: tsf\itflangbaritembutton.htm
tech.root: TSF
ms.assetid: 098a8cdc-ff34-4729-9b34-279c499d40a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemButton, ITfLangBarItemButton interface [Text Services Framework], ITfLangBarItemButton interface [Text Services Framework],described, _tsf_itflangbaritembutton_ref, ctfutb/ITfLangBarItemButton, tsf.itflangbaritembutton
ms.topic: interface
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
 - ITfLangBarItemButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfLangBarItemButton interface


## -description


The <b>ITfLangBarItemButton</b> interface is implemented by a language bar button provider and used by the language bar manager to obtain information about a button item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> passed to <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLangBarItemButton</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemButton</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLangBarItemButton</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-geticon">GetIcon</a>
</td>
<td align="left" width="63%">
Obtains the icon to be displayed for the language bar button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-gettext">GetText</a>
</td>
<td align="left" width="63%">
Obtains the text to be displayed for the button in the language bar.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-initmenu">InitMenu</a>
</td>
<td align="left" width="63%">
Called to allow a language bar button that has the TF_LBI_STYLE_BTN_MENU style to add items to the menu that the language bar will display for the button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-onclick">OnClick</a>
</td>
<td align="left" width="63%">
Called when the user clicks the mouse on a language bar button that has the TF_LBI_STYLE_BTN_BUTTON or TF_LBI_STYLE_BTN_TOGGLE style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect">OnMenuSelect</a>
</td>
<td align="left" width="63%">
Called when the user selects an item in the menu that the language bar displays for the button.

</td>
</tr>
</table> 


## -remarks



A language bar button functions as a pushbutton, toggle button, or a menu on the language bar.

If the button has the TF_LBI_STYLE_BTN_BUTTON style, the button acts as a pushbutton that the user can click with the mouse. When the user clicks the button, <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-onclick">ITfLangBarItemButton::OnClick</a> is called. <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-initmenu">ITfLangBarItemButton::InitMenu</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect">ITfLangBarItemButton::OnMenuSelect</a> are not used.

If the button has the TF_LBI_STYLE_BTN_TOGGLE style, the button functions similar to a check box that the user can select or deselect with the mouse. When the user clicks the button, <b>ITfLangBarItemButton::OnClick</b> is called. <b>ITfLangBarItemButton::InitMenu</b> and <b>ITfLangBarItemButton::OnMenuSelect</b> are not used.

If the button has the TF_LBI_STYLE_BTN_MENU style, the button acts like a top-level menu item. When the user clicks the button, <b>ITfLangBarItemButton::InitMenu</b> is called. If the user selects an item in the menu, <b>ITfLangBarItemButton::OnMenuSelect</b> is called. <b>ITfLangBarItemButton::OnClick</b> is not used.



