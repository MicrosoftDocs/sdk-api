---
UID: NF:ctfutb.ITfLangBarItemMgr.GetItem
title: ITfLangBarItemMgr::GetItem (ctfutb.h)
description: ITfLangBarItemMgr::GetItem method
helpviewer_keywords: ["GetItem","GetItem method [Text Services Framework]","GetItem method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","GetItem method","ITfLangBarItemMgr.GetItem","ITfLangBarItemMgr::GetItem","_tsf_itflangbaritemmgr_getitem_ref","ctfutb/ITfLangBarItemMgr::GetItem","tsf.itflangbaritemmgr_getitem"]
old-location: tsf\itflangbaritemmgr_getitem.htm
tech.root: TSF
ms.assetid: 35895fd7-23d0-416b-98c2-45192edf0a6b
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Text Services Framework], GetItem method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],GetItem method, ITfLangBarItemMgr.GetItem, ITfLangBarItemMgr::GetItem, _tsf_itflangbaritemmgr_getitem_ref, ctfutb/ITfLangBarItemMgr::GetItem, tsf.itflangbaritemmgr_getitem
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
 - ITfLangBarItemMgr::GetItem
 - ctfutb/ITfLangBarItemMgr::GetItem
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
 - ITfLangBarItemMgr.GetItem
---

# ITfLangBarItemMgr::GetItem


## -description

Obtains the ITfLangBarItem interface for an item in the language bar.

## -parameters

### -param rguid [in]

GUID that identifies the item to obtain. This is the item GUID that the item supplies in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>. This identifier can be a custom value or one of the <a href="/windows/desktop/TSF/predefined-lang-bar-items">predefined language bar items</a>.

### -param ppItem [out]

Pointer to an <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a> interface pointer that receives the item interface.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The item cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppItem</i> parameter is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/TSF/predefined-lang-bar-items">Predefined language bar items
      </a>