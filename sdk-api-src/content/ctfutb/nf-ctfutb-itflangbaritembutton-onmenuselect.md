---
UID: NF:ctfutb.ITfLangBarItemButton.OnMenuSelect
title: ITfLangBarItemButton::OnMenuSelect (ctfutb.h)
description: This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style. (ITfLangBarItemButton.OnMenuSelect)
helpviewer_keywords: ["ITfLangBarItemButton interface [Text Services Framework]","OnMenuSelect method","ITfLangBarItemButton.OnMenuSelect","ITfLangBarItemButton::OnMenuSelect","OnMenuSelect","OnMenuSelect method [Text Services Framework]","OnMenuSelect method [Text Services Framework]","ITfLangBarItemButton interface","_tsf_itflangbaritembutton_onmenuselect_ref","ctfutb/ITfLangBarItemButton::OnMenuSelect","tsf.itflangbaritembutton_onmenuselect"]
old-location: tsf\itflangbaritembutton_onmenuselect.htm
tech.root: TSF
ms.assetid: 104cc686-4cb1-4f8e-909b-4c9dfb0b72cc
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemButton interface [Text Services Framework],OnMenuSelect method, ITfLangBarItemButton.OnMenuSelect, ITfLangBarItemButton::OnMenuSelect, OnMenuSelect, OnMenuSelect method [Text Services Framework], OnMenuSelect method [Text Services Framework],ITfLangBarItemButton interface, _tsf_itflangbaritembutton_onmenuselect_ref, ctfutb/ITfLangBarItemButton::OnMenuSelect, tsf.itflangbaritembutton_onmenuselect
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
 - ITfLangBarItemButton::OnMenuSelect
 - ctfutb/ITfLangBarItemButton::OnMenuSelect
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
 - ITfLangBarItemButton.OnMenuSelect
---

# ITfLangBarItemButton::OnMenuSelect


## -description

This method is not used if the button item does not have the TF_LBI_STYLE_BTN_MENU style.

## -parameters

### -param wID [in]

Specifies the identifier of the menu item selected. This is the value passed for the <i>uId</i> parameter in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itfmenu-addmenuitem">ITfMenu::AddMenuItem</a>.

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



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itfmenu-addmenuitem">ITfMenu::AddMenuItem
      </a>
