---
UID: NF:ctfutb.ITfSystemLangBarItem.SetIcon
title: ITfSystemLangBarItem::SetIcon (ctfutb.h)
description: ITfSystemLangBarItem::SetIcon method
helpviewer_keywords: ["ITfSystemLangBarItem interface [Text Services Framework]","SetIcon method","ITfSystemLangBarItem.SetIcon","ITfSystemLangBarItem::SetIcon","SetIcon","SetIcon method [Text Services Framework]","SetIcon method [Text Services Framework]","ITfSystemLangBarItem interface","_tsf_itfsystemlangbaritem_seticon_ref","ctfutb/ITfSystemLangBarItem::SetIcon","tsf.itfsystemlangbaritem_seticon"]
old-location: tsf\itfsystemlangbaritem_seticon.htm
tech.root: TSF
ms.assetid: 6b83e2ec-ac2f-4fd6-8c7c-70b00baafdc1
ms.date: 12/05/2018
ms.keywords: ITfSystemLangBarItem interface [Text Services Framework],SetIcon method, ITfSystemLangBarItem.SetIcon, ITfSystemLangBarItem::SetIcon, SetIcon, SetIcon method [Text Services Framework], SetIcon method [Text Services Framework],ITfSystemLangBarItem interface, _tsf_itfsystemlangbaritem_seticon_ref, ctfutb/ITfSystemLangBarItem::SetIcon, tsf.itfsystemlangbaritem_seticon
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
 - ITfSystemLangBarItem::SetIcon
 - ctfutb/ITfSystemLangBarItem::SetIcon
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
 - ITfSystemLangBarItem.SetIcon
---

# ITfSystemLangBarItem::SetIcon


## -description

Modifies the icon displayed for the system language bar menu.

## -parameters

### -param hIcon [in]

Contains the handle to the new icon.

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
The system language bar menu does not allow its icon to be modified.

</td>
</tr>
</table>

## -remarks

In response to this method, the system language bar menu should call <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemsink-onupdate">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_ICON to force the language bar to obtain the new icon.