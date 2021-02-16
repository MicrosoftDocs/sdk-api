---
UID: NF:ctfutb.ITfLangBarItemMgr.UnadviseItemsSink
title: ITfLangBarItemMgr::UnadviseItemsSink (ctfutb.h)
description: ITfLangBarItemMgr::UnadviseItemsSink method
helpviewer_keywords: ["ITfLangBarItemMgr interface [Text Services Framework]","UnadviseItemsSink method","ITfLangBarItemMgr.UnadviseItemsSink","ITfLangBarItemMgr::UnadviseItemsSink","UnadviseItemsSink","UnadviseItemsSink method [Text Services Framework]","UnadviseItemsSink method [Text Services Framework]","ITfLangBarItemMgr interface","_tsf_itflangbaritemmgr_unadviseitemssink_ref","ctfutb/ITfLangBarItemMgr::UnadviseItemsSink","tsf.itflangbaritemmgr_unadviseitemssink"]
old-location: tsf\itflangbaritemmgr_unadviseitemssink.htm
tech.root: TSF
ms.assetid: e15fb870-bedc-412d-9561-4db6c0515799
ms.date: 12/05/2018
ms.keywords: ITfLangBarItemMgr interface [Text Services Framework],UnadviseItemsSink method, ITfLangBarItemMgr.UnadviseItemsSink, ITfLangBarItemMgr::UnadviseItemsSink, UnadviseItemsSink, UnadviseItemsSink method [Text Services Framework], UnadviseItemsSink method [Text Services Framework],ITfLangBarItemMgr interface, _tsf_itflangbaritemmgr_unadviseitemssink_ref, ctfutb/ITfLangBarItemMgr::UnadviseItemsSink, tsf.itflangbaritemmgr_unadviseitemssink
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
 - ITfLangBarItemMgr::UnadviseItemsSink
 - ctfutb/ITfLangBarItemMgr::UnadviseItemsSink
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
 - ITfLangBarItemMgr.UnadviseItemsSink
---

# ITfLangBarItemMgr::UnadviseItemsSink


## -description

Removes one or more language bar item event sinks.

## -parameters

### -param ulCount [in]

Contains the number of advise sinks to install.

### -param pdwCookie [in]

Pointer to an array of <b>DWORD</b>s that identify the advise sinks to remove. These cookies are obtained when the advise sinks are installed with <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">ITfLangBarItemMgr::AdviseItemsSink</a>. This array must be at least <i>ulCount</i> elements in length.

## -returns

This method has no return values.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr">ITfLangBarItemMgr</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemsink">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-adviseitemssink">ITfLangBarItemMgr::AdviseItemsSink
      </a>