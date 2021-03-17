---
UID: NF:ctfutb.ITfLangBarItemSink.OnUpdate
title: ITfLangBarItemSink::OnUpdate (ctfutb.h)
description: ITfLangBarItemSink::OnUpdate method
helpviewer_keywords: ["ITfLangBarItemSink interface [Text Services Framework]","OnUpdate method","ITfLangBarItemSink.OnUpdate","ITfLangBarItemSink::OnUpdate","OnUpdate","OnUpdate method [Text Services Framework]","OnUpdate method [Text Services Framework]","ITfLangBarItemSink interface","_tsf_itflangbaritemsink_onupdate_ref","ctfutb/ITfLangBarItemSink::OnUpdate","tsf.itflangbaritemsink_onupdate"]
old-location: tsf\itflangbaritemsink_onupdate.htm
tech.root: TSF
ms.assetid: f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemSink interface [Text Services Framework],OnUpdate method, ITfLangBarItemSink.OnUpdate, ITfLangBarItemSink::OnUpdate, OnUpdate, OnUpdate method [Text Services Framework], OnUpdate method [Text Services Framework],ITfLangBarItemSink interface, _tsf_itflangbaritemsink_onupdate_ref, ctfutb/ITfLangBarItemSink::OnUpdate, tsf.itflangbaritemsink_onupdate
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
 - ITfLangBarItemSink::OnUpdate
 - ctfutb/ITfLangBarItemSink::OnUpdate
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
 - ITfLangBarItemSink.OnUpdate
---

# ITfLangBarItemSink::OnUpdate


## -description

Notifies the language bar of a change in a language bar item.

## -parameters

### -param dwFlags [in]

Contains a set of flags that indicate changes in the language bar item. This can be a combination of one or more of the <a href="/windows/desktop/TSF/tf-lbi--constants">TF_LBI_*</a> values.

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

## -remarks

A language bar item should call this method when the internal state of the item changes. TSF will update the language bar user interface appropriately.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink">ITfLangBarItemSink</a>



<a href="/windows/desktop/TSF/tf-lbi--constants">TF_LBI_* Constants</a>