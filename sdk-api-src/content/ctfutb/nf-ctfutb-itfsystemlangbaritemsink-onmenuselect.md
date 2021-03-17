---
UID: NF:ctfutb.ITfSystemLangBarItemSink.OnMenuSelect
title: ITfSystemLangBarItemSink::OnMenuSelect (ctfutb.h)
description: ITfSystemLangBarItemSink::OnMenuSelect method
helpviewer_keywords: ["ITfSystemLangBarItemSink interface [Text Services Framework]","OnMenuSelect method","ITfSystemLangBarItemSink.OnMenuSelect","ITfSystemLangBarItemSink::OnMenuSelect","OnMenuSelect","OnMenuSelect method [Text Services Framework]","OnMenuSelect method [Text Services Framework]","ITfSystemLangBarItemSink interface","_tsf_itfsystemlangbaritemsink_onmenuselect_ref","ctfutb/ITfSystemLangBarItemSink::OnMenuSelect","tsf.itfsystemlangbaritemsink_onmenuselect"]
old-location: tsf\itfsystemlangbaritemsink_onmenuselect.htm
tech.root: TSF
ms.assetid: 43c20f95-64b5-458a-8469-0d8b284b66dd
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItemSink interface [Text Services Framework],OnMenuSelect method, ITfSystemLangBarItemSink.OnMenuSelect, ITfSystemLangBarItemSink::OnMenuSelect, OnMenuSelect, OnMenuSelect method [Text Services Framework], OnMenuSelect method [Text Services Framework],ITfSystemLangBarItemSink interface, _tsf_itfsystemlangbaritemsink_onmenuselect_ref, ctfutb/ITfSystemLangBarItemSink::OnMenuSelect, tsf.itfsystemlangbaritemsink_onmenuselect
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
 - ITfSystemLangBarItemSink::OnMenuSelect
 - ctfutb/ITfSystemLangBarItemSink::OnMenuSelect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfSystemLangBarItemSink.OnMenuSelect
---

# ITfSystemLangBarItemSink::OnMenuSelect


## -description

Called when the user selects an item in the system menu added by the system language bar menu extension.

## -parameters

### -param wID [in]

Specifies the identifier of the menu item selected. This is the value passed for <i>uId</i> in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itfmenu-addmenuitem">ITfMenu::AddMenuItem</a>.

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

<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itfmenu-addmenuitem">ITfMenu::AddMenuItem
      </a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink">ITfSystemLangBarItemSink</a>