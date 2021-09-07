---
UID: NF:ctfutb.ITfLangBarItemMgr.AdviseItemsSink
title: ITfLangBarItemMgr::AdviseItemsSink (ctfutb.h)
description: ITfLangBarItemMgr::AdviseItemsSink method
helpviewer_keywords: ["AdviseItemsSink","AdviseItemsSink method [Text Services Framework]","AdviseItemsSink method [Text Services Framework]","ITfLangBarItemMgr interface","ITfLangBarItemMgr interface [Text Services Framework]","AdviseItemsSink method","ITfLangBarItemMgr.AdviseItemsSink","ITfLangBarItemMgr::AdviseItemsSink","_tsf_itflangbaritemmgr_adviseitemssink_ref","ctfutb/ITfLangBarItemMgr::AdviseItemsSink","tsf.itflangbaritemmgr_adviseitemssink"]
old-location: tsf\itflangbaritemmgr_adviseitemssink.htm
tech.root: TSF
ms.assetid: c0a3e86b-487b-410a-8bba-c2b5126126d2
ms.date: 12/05/2018
ms.keywords: AdviseItemsSink, AdviseItemsSink method [Text Services Framework], AdviseItemsSink method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],AdviseItemsSink method, ITfLangBarItemMgr.AdviseItemsSink, ITfLangBarItemMgr::AdviseItemsSink, _tsf_itflangbaritemmgr_adviseitemssink_ref, ctfutb/ITfLangBarItemMgr::AdviseItemsSink, tsf.itflangbaritemmgr_adviseitemssink
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
 - ITfLangBarItemMgr::AdviseItemsSink
 - ctfutb/ITfLangBarItemMgr::AdviseItemsSink
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
 - ITfLangBarItemMgr.AdviseItemsSink
---

# ITfLangBarItemMgr::AdviseItemsSink


## -description

Installs one or more language bar item event sinks for one or more language bar items.

## -parameters

### -param ulCount [in]

Contains the number of advise sinks to install.

### -param ppunk [in]

Pointer to an array of <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink">ITfLangBarItemSink</a> objects to install. This array must be at least <i>ulCount</i> elements in length.

### -param pguidItem [in]

Pointer to an array of <b>GUID</b>s that identify the items to install the advise sinks for. These are the item <b>GUID</b>s that the item supplies in <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>. This array must be at least <i>ulCount</i> elements in length.

### -param pdwCookie [out]

Pointer to an array of <b>DWORD</b>s that receive the corresponding advise sink identification cookies. These cookies identify the advise sinks when they are removed with the <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemsink">ITfLangBarItemMgr::UnadviseItemSink</a> or <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemssink">ITfLangBarItemMgr::UnadviseItemsSink</a> method. This array must be at least <i>ulCount</i> elements in length.

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

<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo">ITfLangBarItem::GetInfo</a>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-unadviseitemsink">ITfLangBarItemMgr::UnadviseItemSink
      </a>



<b>ITfLangBarItemMgr::UnadviseItemsSink
      </b>



<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink">ITfLangBarItemSink</a>