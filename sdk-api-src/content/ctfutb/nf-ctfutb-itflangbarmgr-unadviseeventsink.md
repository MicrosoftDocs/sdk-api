---
UID: NF:ctfutb.ITfLangBarMgr.UnadviseEventSink
title: ITfLangBarMgr::UnadviseEventSink (ctfutb.h)
description: ITfLangBarMgr::UnadviseEventSink method
helpviewer_keywords: ["ITfLangBarMgr interface [Text Services Framework]","UnadviseEventSink method","ITfLangBarMgr.UnadviseEventSink","ITfLangBarMgr::UnadviseEventSink","UnadviseEventSink","UnadviseEventSink method [Text Services Framework]","UnadviseEventSink method [Text Services Framework]","ITfLangBarMgr interface","_tsf_itflangbarmgr_unadviseeventsink_ref","ctfutb/ITfLangBarMgr::UnadviseEventSink","tsf.itflangbarmgr_unadviseeventsink"]
old-location: tsf\itflangbarmgr_unadviseeventsink.htm
tech.root: TSF
ms.assetid: 29dc5276-04fa-4219-a64d-10d775d73fdd
ms.date: 12/05/2018
ms.keywords: ITfLangBarMgr interface [Text Services Framework],UnadviseEventSink method, ITfLangBarMgr.UnadviseEventSink, ITfLangBarMgr::UnadviseEventSink, UnadviseEventSink, UnadviseEventSink method [Text Services Framework], UnadviseEventSink method [Text Services Framework],ITfLangBarMgr interface, _tsf_itflangbarmgr_unadviseeventsink_ref, ctfutb/ITfLangBarMgr::UnadviseEventSink, tsf.itflangbarmgr_unadviseeventsink
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
 - ITfLangBarMgr::UnadviseEventSink
 - ctfutb/ITfLangBarMgr::UnadviseEventSink
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
 - ITfLangBarMgr.UnadviseEventSink
---

# ITfLangBarMgr::UnadviseEventSink


## -description

Uninstalls an advise event sink.

## -parameters

### -param dwCookie [in]

A DWORD value that identifies the advise event sink to uninstall. This value is provided by a previous call to <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">ITfLangBarMgr::AdviseEventSink</a>.

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

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbarmgr">ITfLangBarMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">ITfLangBarMgr::AdviseEventSink
      </a>



<a href="/windows/desktop/TSF/thread-manager">Thread Manager</a>