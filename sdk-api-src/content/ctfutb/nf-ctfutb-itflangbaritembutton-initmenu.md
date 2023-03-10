---
UID: NF:ctfutb.ITfLangBarItemButton.InitMenu
title: ITfLangBarItemButton::InitMenu (ctfutb.h)
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style. (ITfLangBarItemButton.InitMenu)
helpviewer_keywords: ["ITfLangBarItemButton interface [Text Services Framework]","InitMenu method","ITfLangBarItemButton.InitMenu","ITfLangBarItemButton::InitMenu","InitMenu","InitMenu method [Text Services Framework]","InitMenu method [Text Services Framework]","ITfLangBarItemButton interface","_tsf_itflangbaritembutton_initmenu_ref","ctfutb/ITfLangBarItemButton::InitMenu","tsf.itflangbaritembutton_initmenu"]
old-location: tsf\itflangbaritembutton_initmenu.htm
tech.root: TSF
ms.assetid: 6f9debf8-1c25-4228-abd2-2b2a099cf5cd
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemButton interface [Text Services Framework],InitMenu method, ITfLangBarItemButton.InitMenu, ITfLangBarItemButton::InitMenu, InitMenu, InitMenu method [Text Services Framework], InitMenu method [Text Services Framework],ITfLangBarItemButton interface, _tsf_itflangbaritembutton_initmenu_ref, ctfutb/ITfLangBarItemButton::InitMenu, tsf.itflangbaritembutton_initmenu
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
 - ITfLangBarItemButton::InitMenu
 - ctfutb/ITfLangBarItemButton::InitMenu
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
 - ITfLangBarItemButton.InitMenu
---

# ITfLangBarItemButton::InitMenu


## -description

This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.

## -parameters

### -param pMenu [in]

Pointer to an <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu</a> interface that the language bar button uses to add items to the menu that the language bar displays for the button.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritembutton">ITfLangBarItemButton</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu
      </a>
