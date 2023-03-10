---
UID: NF:ctfutb.ITfLangBarItemMgr.AdviseItemSink
title: ITfLangBarItemMgr::AdviseItemSink (ctfutb.h)
description: ITfLangBarItemMgr::AdviseItemSink method
helpviewer_keywords: ["AdviseItemSink","AdviseItemSink method [Text Services Framework]","AdviseItemSink method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","AdviseItemSink method","ITfLangBarItemMgr.AdviseItemSink","ITfLangBarItemMgr::AdviseItemSink","_tsf_itflangbaritemmgr_adviseitemsink_ref","ctfutb/ITfLangBarItemMgr::AdviseItemSink","tsf.itflangbaritemmgr_adviseitemsink"]
old-location: tsf\itflangbaritemmgr_adviseitemsink.htm
tech.root: TSF
ms.assetid: c01d80eb-9156-4fbf-98ff-7f06b145e72f
ms.date: 12/05/2018
ms.keywords: AdviseItemSink, AdviseItemSink method [Text Services Framework], AdviseItemSink method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],AdviseItemSink method, ITfLangBarItemMgr.AdviseItemSink, ITfLangBarItemMgr::AdviseItemSink, _tsf_itflangbaritemmgr_adviseitemsink_ref, ctfutb/ITfLangBarItemMgr::AdviseItemSink, tsf.itflangbaritemmgr_adviseitemsink
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
 - ITfLangBarItemMgr::AdviseItemSink
 - ctfutb/ITfLangBarItemMgr::AdviseItemSink
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
 - ITfLangBarItemMgr.AdviseItemSink
---

# ITfLangBarItemMgr::AdviseItemSink


## -description

Installs a language bar item event sink for a language bar item.

## -parameters

### -param punk [in]

Pointer to the <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink">ITfLangBarItemSink</a> object to install.

### -param pdwCookie [out]

Pointer to a <b>DWORD</b> that receives an advise sink identification cookie. This cookie identifies the advise sink when it is removed with the <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemsink">ITfLangBarItemMgr::UnadviseItemSink</a> or <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemssink">ITfLangBarItemMgr::UnadviseItemsSink</a> method.

### -param rguidItem [in]

Contains the <b>GUID</b> that identifies the item to install the advise sink for. This is the item <b>GUID</b> that the item supplies in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>. This can be a custom value or one of the <a href="/windows/desktop/TSF/predefined-lang-bar-items">predefined language bar items</a>.

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
<i>rguidItem</i> is invalid.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>punk</i> and/or <i>pdwCookie</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemsink">ITfLangBarItemMgr::UnadviseItemSink
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemssink">ITfLangBarItemMgr::UnadviseItemsSink
      </a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink">ITfLangBarItemSink</a>



<a href="/windows/desktop/TSF/predefined-lang-bar-items">Predefined language bar items
      </a>