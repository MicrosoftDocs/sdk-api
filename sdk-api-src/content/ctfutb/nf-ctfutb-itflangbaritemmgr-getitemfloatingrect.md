---
UID: NF:ctfutb.ITfLangBarItemMgr.GetItemFloatingRect
title: ITfLangBarItemMgr::GetItemFloatingRect (ctfutb.h)
description: ITfLangBarItemMgr::GetItemFloatingRect method
helpviewer_keywords: ["GetItemFloatingRect","GetItemFloatingRect method [Text Services Framework]","GetItemFloatingRect method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","GetItemFloatingRect method","ITfLangBarItemMgr.GetItemFloatingRect","ITfLangBarItemMgr::GetItemFloatingRect","_tsf_itflangbaritemmgr_getitemfloatingrect_ref","ctfutb/ITfLangBarItemMgr::GetItemFloatingRect","tsf.itflangbaritemmgr_getitemfloatingrect"]
old-location: tsf\itflangbaritemmgr_getitemfloatingrect.htm
tech.root: TSF
ms.assetid: 56f30b8e-9e71-4b4e-a7df-e83d24cab297
ms.date: 12/05/2018
ms.keywords: GetItemFloatingRect, GetItemFloatingRect method [Text Services Framework], GetItemFloatingRect method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],GetItemFloatingRect method, ITfLangBarItemMgr.GetItemFloatingRect, ITfLangBarItemMgr::GetItemFloatingRect, _tsf_itflangbaritemmgr_getitemfloatingrect_ref, ctfutb/ITfLangBarItemMgr::GetItemFloatingRect, tsf.itflangbaritemmgr_getitemfloatingrect
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
 - ITfLangBarItemMgr::GetItemFloatingRect
 - ctfutb/ITfLangBarItemMgr::GetItemFloatingRect
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
 - ITfLangBarItemMgr.GetItemFloatingRect
---

# ITfLangBarItemMgr::GetItemFloatingRect


## -description

Obtains the bounding rectangle of an item on the language bar.

## -parameters

### -param dwThreadId [in]

Not currently used. Must be zero.

### -param rguid [in]

Contains the <b>GUID</b> that identifies the item to obtain the bounding rectangle for. This is the item <b>GUID</b> that the item supplies in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>. This can be a custom value or one of the <a href="/windows/desktop/TSF/predefined-lang-bar-items">predefined language bar items</a>.

### -param prc [out]

Pointer to a <b>RECT</b> structure that receives the bounding rectangle in screen coordinates.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>prc</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/TSF/predefined-lang-bar-items">Predefined language bar items
      </a>