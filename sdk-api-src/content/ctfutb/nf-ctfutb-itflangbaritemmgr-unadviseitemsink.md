---
UID: NF:ctfutb.ITfLangBarItemMgr.UnadviseItemSink
title: ITfLangBarItemMgr::UnadviseItemSink (ctfutb.h)
description: ITfLangBarItemMgr::UnadviseItemSink method
helpviewer_keywords: ["ITfLangBarItemMgr interface [Text Services Framework]","UnadviseItemSink method","ITfLangBarItemMgr.UnadviseItemSink","ITfLangBarItemMgr::UnadviseItemSink","UnadviseItemSink","UnadviseItemSink method [Text Services Framework]","UnadviseItemSink method [Text Services Framework]","ITfLangBarItemMgr interface","_tsf_itflangbaritemmgr_unadviseitemsink_ref","ctfutb/ITfLangBarItemMgr::UnadviseItemSink","tsf.itflangbaritemmgr_unadviseitemsink"]
old-location: tsf\itflangbaritemmgr_unadviseitemsink.htm
tech.root: TSF
ms.assetid: 20a0f69b-950e-4ad7-9357-74f0b4a75c6b
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemMgr interface [Text Services Framework],UnadviseItemSink method, ITfLangBarItemMgr.UnadviseItemSink, ITfLangBarItemMgr::UnadviseItemSink, UnadviseItemSink, UnadviseItemSink method [Text Services Framework], UnadviseItemSink method [Text Services Framework],ITfLangBarItemMgr interface, _tsf_itflangbaritemmgr_unadviseitemsink_ref, ctfutb/ITfLangBarItemMgr::UnadviseItemSink, tsf.itflangbaritemmgr_unadviseitemsink
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
 - ITfLangBarItemMgr::UnadviseItemSink
 - ctfutb/ITfLangBarItemMgr::UnadviseItemSink
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
 - ITfLangBarItemMgr.UnadviseItemSink
---

# ITfLangBarItemMgr::UnadviseItemSink


## -description

Removes a language bar item event sink.

## -parameters

### -param dwCookie [in]

Contains a <i>DWORD</i> that identifies the advise sink to remove. This cookie is obtained when the advise sink is installed with <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">ITfLangBarItemMgr::AdviseItemsSink</a>.

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

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">ITfLangBarItemMgr::AdviseItemsSink
      </a>