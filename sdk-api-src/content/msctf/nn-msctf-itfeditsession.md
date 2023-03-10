---
UID: NN:msctf.ITfEditSession
title: ITfEditSession (msctf.h)
description: The ITfEditSession interface is implemented by a text service and used by the TSF manager to read and/or modify the text and properties of a context.
helpviewer_keywords: ["ITfEditSession","ITfEditSession interface [Text Services Framework]","ITfEditSession interface [Text Services Framework]","described","_tsf_itfeditsession_ref","msctf/ITfEditSession","tsf.itfeditsession"]
old-location: tsf\itfeditsession.htm
tech.root: TSF
ms.assetid: b9d4718a-42a6-4be5-9f57-1a392cd98469
ms.date: 12/05/2018
ms.keywords: ITfEditSession, ITfEditSession interface [Text Services Framework], ITfEditSession interface [Text Services Framework],described, _tsf_itfeditsession_ref, msctf/ITfEditSession, tsf.itfeditsession
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Tipskins.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfEditSession
 - msctf/ITfEditSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tipskins.dll
api_name:
 - ITfEditSession
---

# ITfEditSession interface


## -description

The <b>ITfEditSession</b> interface is implemented by a text service and used by the TSF manager to read and/or modify the text and properties of a context.

## -inheritance

The <b>ITfEditSession</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfEditSession</b> also has these types of members:

## -remarks

A text service initiates an edit session by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">ITfContext::RequestEditSession</a>, passing a pointer to the <b>ITfEditSession</b> interface. When the edit session is granted, the TSF manager calls <b>DoEditSession</b>.

If the context is destroyed before the application grants a lock, or if the calling text service is deactivated before a lock is granted, the <b>DoEditSession</b> method is not called. For this reason, a text service should put cleanup operations for an edit session in the <b>ITfEditSession</b> interface destructor rather than in the <b>DoEditSession</b> method.

## -see-also

<a href="/windows/desktop/TSF/edit-sessions">Edit Sessions</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-requesteditsession">ITfContext::RequestEditSession
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
