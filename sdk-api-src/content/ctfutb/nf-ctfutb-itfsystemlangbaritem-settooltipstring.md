---
UID: NF:ctfutb.ITfSystemLangBarItem.SetTooltipString
title: ITfSystemLangBarItem::SetTooltipString (ctfutb.h)
description: ITfSystemLangBarItem::SetTooltipString method
helpviewer_keywords: ["ITfSystemLangBarItem interface [Text Services Framework]","SetTooltipString method","ITfSystemLangBarItem.SetTooltipString","ITfSystemLangBarItem::SetTooltipString","SetTooltipString","SetTooltipString method [Text Services Framework]","SetTooltipString method [Text Services Framework]","ITfSystemLangBarItem interface","_tsf_itfsystemlangbaritem_settooltipstring_ref","ctfutb/ITfSystemLangBarItem::SetTooltipString","tsf.itfsystemlangbaritem_settooltipstring"]
old-location: tsf\itfsystemlangbaritem_settooltipstring.htm
tech.root: TSF
ms.assetid: 6917fcd1-acce-4e5d-b04f-ee8ea69e71b4
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItem interface [Text Services Framework],SetTooltipString method, ITfSystemLangBarItem.SetTooltipString, ITfSystemLangBarItem::SetTooltipString, SetTooltipString, SetTooltipString method [Text Services Framework], SetTooltipString method [Text Services Framework],ITfSystemLangBarItem interface, _tsf_itfsystemlangbaritem_settooltipstring_ref, ctfutb/ITfSystemLangBarItem::SetTooltipString, tsf.itfsystemlangbaritem_settooltipstring
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
 - ITfSystemLangBarItem::SetTooltipString
 - ctfutb/ITfSystemLangBarItem::SetTooltipString
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
 - ITfSystemLangBarItem.SetTooltipString
---

# ITfSystemLangBarItem::SetTooltipString


## -description

Modifies the tooltip text displayed for the system language bar menu.

## -parameters

### -param pchToolTip [in]

A string that appears as a tooltip.

### -param cch [in]

Size, in characters, of the string.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The tooltip string for the system language bar menu cannot be modified.

</td>
</tr>
</table>

## -remarks

In response to this method, the system language bar menu should call <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemsink-onupdate">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_TOOLTIP to force the language bar to obtain the new tooltip text.