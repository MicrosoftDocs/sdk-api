---
UID: NN:ctfutb.ITfLangBarItemButton
title: ITfLangBarItemButton (ctfutb.h)
description: The ITfLangBarItemButton interface is implemented by a language bar button provider and used by the language bar manager to obtain information about a button item on the language bar.
helpviewer_keywords: ["ITfLangBarItemButton","ITfLangBarItemButton interface [Text Services Framework]","ITfLangBarItemButton interface [Text Services Framework]","described","_tsf_itflangbaritembutton_ref","ctfutb/ITfLangBarItemButton","tsf.itflangbaritembutton"]
old-location: tsf\itflangbaritembutton.htm
tech.root: TSF
ms.assetid: 098a8cdc-ff34-4729-9b34-279c499d40a8
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemButton, ITfLangBarItemButton interface [Text Services Framework], ITfLangBarItemButton interface [Text Services Framework],described, _tsf_itflangbaritembutton_ref, ctfutb/ITfLangBarItemButton, tsf.itflangbaritembutton
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
 - ITfLangBarItemButton
 - ctfutb/ITfLangBarItemButton
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
 - ITfLangBarItemButton
---

# ITfLangBarItemButton interface


## -description

The <b>ITfLangBarItemButton</b> interface is implemented by a language bar button provider and used by the language bar manager to obtain information about a button item on the language bar.

The language bar manager obtains an instance of this interface by calling QueryInterface on the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> passed to <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem">ITfLangBarItemMgr::AddItem</a>.

## -inheritance

The <b>ITfLangBarItemButton</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarItemButton</b> also has these types of members:

## -remarks

A language bar button functions as a pushbutton, toggle button, or a menu on the language bar.

If the button has the TF_LBI_STYLE_BTN_BUTTON style, the button acts as a pushbutton that the user can click with the mouse. When the user clicks the button, <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-onclick">ITfLangBarItemButton::OnClick</a> is called. <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-initmenu">ITfLangBarItemButton::InitMenu</a> and <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect">ITfLangBarItemButton::OnMenuSelect</a> are not used.

If the button has the TF_LBI_STYLE_BTN_TOGGLE style, the button functions similar to a check box that the user can select or deselect with the mouse. When the user clicks the button, <b>ITfLangBarItemButton::OnClick</b> is called. <b>ITfLangBarItemButton::InitMenu</b> and <b>ITfLangBarItemButton::OnMenuSelect</b> are not used.

If the button has the TF_LBI_STYLE_BTN_MENU style, the button acts like a top-level menu item. When the user clicks the button, <b>ITfLangBarItemButton::InitMenu</b> is called. If the user selects an item in the menu, <b>ITfLangBarItemButton::OnMenuSelect</b> is called. <b>ITfLangBarItemButton::OnClick</b> is not used.
