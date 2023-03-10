---
UID: NF:ctfutb.ITfLangBarItemMgr.AddItem
title: ITfLangBarItemMgr::AddItem (ctfutb.h)
description: ITfLangBarItemMgr::AddItem method
helpviewer_keywords: ["AddItem","AddItem method [Text Services Framework]","AddItem method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","AddItem method","ITfLangBarItemMgr.AddItem","ITfLangBarItemMgr::AddItem","_tsf_itflangbaritemmgr_additem_ref","ctfutb/ITfLangBarItemMgr::AddItem","tsf.itflangbaritemmgr_additem"]
old-location: tsf\itflangbaritemmgr_additem.htm
tech.root: TSF
ms.assetid: c9a36b2c-e7ea-4932-928e-05dd05ca02ca
ms.date: 12/05/2018
ms.keywords: AddItem, AddItem method [Text Services Framework], AddItem method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],AddItem method, ITfLangBarItemMgr.AddItem, ITfLangBarItemMgr::AddItem, _tsf_itflangbaritemmgr_additem_ref, ctfutb/ITfLangBarItemMgr::AddItem, tsf.itflangbaritemmgr_additem
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
 - ITfLangBarItemMgr::AddItem
 - ctfutb/ITfLangBarItemMgr::AddItem
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
 - ITfLangBarItemMgr.AddItem
---

# ITfLangBarItemMgr::AddItem


## -description

Adds an item to the language bar.

## -parameters

### -param punk [in]

Pointer to the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> object to add to the language bar. 

Starting with Windows 8, only the first item that returns GUID_LBI_INPUTMODE (from [GetInfo](/windows/win32/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo)) is shown. For more information, see [Third-party input method editors](https://docs.microsoft.com/en-us/windows/win32/w8cookbook/third-party-input-method-editors#manifestation) in the Compatibility cookbook for Windows.

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
The method was successful (silently ignored calls also return this status).

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>punk</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>
