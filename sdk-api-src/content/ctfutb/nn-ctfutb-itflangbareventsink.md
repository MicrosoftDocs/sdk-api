---
UID: NN:ctfutb.ITfLangBarEventSink
title: ITfLangBarEventSink (ctfutb.h)
description: The ITfLangBarEventSink interface is implemented by an application or text service and used by the language bar to supply notifications of certain events that occur in the language bar.
helpviewer_keywords: ["ITfLangBarEventSink","ITfLangBarEventSink interface [Text Services Framework]","ITfLangBarEventSink interface [Text Services Framework]","described","_tsf_itflangbareventsink_ref","ctfutb/ITfLangBarEventSink","tsf.itflangbareventsink"]
old-location: tsf\itflangbareventsink.htm
tech.root: TSF
ms.assetid: 2ef8b8ff-6549-41f8-baf3-3c5b8e2411a3
ms.date: 12/05/2018
ms.keywords: ITfLangBarEventSink, ITfLangBarEventSink interface [Text Services Framework], ITfLangBarEventSink interface [Text Services Framework],described, _tsf_itflangbareventsink_ref, ctfutb/ITfLangBarEventSink, tsf.itflangbareventsink
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
 - ITfLangBarEventSink
 - ctfutb/ITfLangBarEventSink
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
 - ITfLangBarEventSink
---

# ITfLangBarEventSink interface


## -description

The <b>ITfLangBarEventSink</b> interface is implemented by an application or text service and used by the language bar to supply notifications of certain events that occur in the language bar. The application or text service installs this event sink by calling <a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">ITfLangBarMgr::AdviseEventSink</a>.

## -inheritance

The <b>ITfLangBarEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfLangBarEventSink</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-adviseeventsink">ITfLangBarMgr::AdviseEventSink
      </a>



<a href="/windows/desktop/api/ctfutb/nf-ctfutb-itflangbarmgr-showfloating">ITfLangBarMgr::ShowFloating
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
