---
UID: NF:ctfutb.ITfLangBarEventSink.ShowFloating
title: ITfLangBarEventSink::ShowFloating (ctfutb.h)
description: ITfLangBarEventSink::ShowFloating method
helpviewer_keywords: ["ITfLangBarEventSink interface [Text Services Framework]","ShowFloating method","ITfLangBarEventSink.ShowFloating","ITfLangBarEventSink::ShowFloating","ShowFloating","ShowFloating method [Text Services Framework]","ShowFloating method [Text Services Framework]","ITfLangBarEventSink interface","_tsf_itflangbareventsink_showfloating_ref","ctfutb/ITfLangBarEventSink::ShowFloating","tsf.itflangbareventsink_showfloating"]
old-location: tsf\itflangbareventsink_showfloating.htm
tech.root: TSF
ms.assetid: f667762a-f276-4311-827e-f89eca7eba1e
ms.date: 12/05/2018
ms.keywords: ITfLangBarEventSink interface [Text Services Framework],ShowFloating method, ITfLangBarEventSink.ShowFloating, ITfLangBarEventSink::ShowFloating, ShowFloating, ShowFloating method [Text Services Framework], ShowFloating method [Text Services Framework],ITfLangBarEventSink interface, _tsf_itflangbareventsink_showfloating_ref, ctfutb/ITfLangBarEventSink::ShowFloating, tsf.itflangbareventsink_showfloating
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
req.dll: Msutb.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfLangBarEventSink::ShowFloating
 - ctfutb/ITfLangBarEventSink::ShowFloating
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msutb.dll
api_name:
 - ITfLangBarEventSink.ShowFloating
---

# ITfLangBarEventSink::ShowFloating


## -description

Called when [ITfLangBarMgr::ShowFloating](nf-ctfutb-itflangbarmgr-showfloating.md) is called.

## -parameters

### -param dwFlags [in]

Contains the <a href="/windows/desktop/TSF/tf-sft--constants">TF_SFT_*</a> values passed to <b>ITfLangBarMgr::ShowFloating</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbareventsink">ITfLangBarEventSink</a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-showfloating">ITfLangBarMgr::ShowFloating
      </a>



<a href="/windows/desktop/TSF/tf-sft--constants">TF_SFT_* Constants
      </a>