---
UID: NF:ctfutb.ITfLangBarMgr.AdviseEventSink
title: ITfLangBarMgr::AdviseEventSink (ctfutb.h)
description: The ITfLangBarMgr::AdviseEventSink method advises a sink about a language bar event.
helpviewer_keywords: ["AdviseEventSink","AdviseEventSink method [Text Services Framework]","AdviseEventSink method [Text Services Framework]","ITfLangBarMgr interface","ITfLangBarMgr interface [Text Services Framework]","AdviseEventSink method","ITfLangBarMgr.AdviseEventSink","ITfLangBarMgr::AdviseEventSink","_tsf_itflangbarmgr_adviseeventsink_ref","ctfutb/ITfLangBarMgr::AdviseEventSink","tsf.itflangbarmgr_adviseeventsink"]
old-location: tsf\itflangbarmgr_adviseeventsink.htm
tech.root: TSF
ms.assetid: 8ac607fd-b2c4-4441-8738-c64c25b6c586
ms.date: 12/05/2018
ms.keywords: AdviseEventSink, AdviseEventSink method [Text Services Framework], AdviseEventSink method [Text Services Framework],ITfLangBarMgr interface, ITfLangBarMgr interface [Text Services Framework],AdviseEventSink method, ITfLangBarMgr.AdviseEventSink, ITfLangBarMgr::AdviseEventSink, _tsf_itflangbarmgr_adviseeventsink_ref, ctfutb/ITfLangBarMgr::AdviseEventSink, tsf.itflangbarmgr_adviseeventsink
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
 - ITfLangBarMgr::AdviseEventSink
 - ctfutb/ITfLangBarMgr::AdviseEventSink
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
 - ITfLangBarMgr.AdviseEventSink
---

# ITfLangBarMgr::AdviseEventSink


## -description

The <b>ITfLangBarMgr::AdviseEventSink</b> method advises a sink about a language bar event.

## -parameters

### -param pSink [in]

Sink object to advise about the event.

### -param hwnd [in]

Reserved; must be <b>NULL</b>.

### -param dwFlags [in]

Reserved; must be 0.

### -param pdwCookie [in]

Pointer to an identifier for the connection.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pSink</i> is invalid.

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

<i>pdwCookie</i> receives an identifier that should be passed to <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-unadviseeventsink">ITfLangBarMgr::UnadviseEventSink</a> when the event sink is no longer required.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbarmgr">ITfLangBarMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-unadviseeventsink">ITfLangBarMgr::UnadviseEventSink
      </a>



<a href="/windows/desktop/TSF/thread-manager">Thread Manager</a>