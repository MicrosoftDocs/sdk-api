---
UID: NN:msctf.ITfThreadMgr
title: ITfThreadMgr (msctf.h)
description: The ITfThreadMgr defines the primary object implemented by the TSF manager. ITfThreadMgr is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.
helpviewer_keywords: ["ITfThreadMgr","ITfThreadMgr interface [Text Services Framework]","ITfThreadMgr interface [Text Services Framework]","described","_tsf_itfthreadmgr_ref","msctf/ITfThreadMgr","tsf.itfthreadmgr"]
old-location: tsf\itfthreadmgr.htm
tech.root: TSF
ms.assetid: 3a2ba59c-3565-4f54-ac10-923dcb4882cb
ms.date: 12/05/2018
ms.keywords: ITfThreadMgr, ITfThreadMgr interface [Text Services Framework], ITfThreadMgr interface [Text Services Framework],described, _tsf_itfthreadmgr_ref, msctf/ITfThreadMgr, tsf.itfthreadmgr
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfThreadMgr
 - msctf/ITfThreadMgr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfThreadMgr
---

# ITfThreadMgr interface


## -description

The <b>ITfThreadMgr</b> defines the primary object implemented by the TSF manager. <b>ITfThreadMgr</b> is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.

## -inheritance

The <b>ITfThreadMgr</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfThreadMgr</b> also has these types of members:

## -remarks

An application obtains a pointer to this interface by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with CLSID_TF_ThreadMgr as demonstrated below.

A text service receives a pointer to this interface in its <a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate</a> method.


#### Examples


```cpp

HRESULT hr;
ITfThreadMgr* pThreadMgr;

hr = CoCreateInstance(  CLSID_TF_ThreadMgr, 
                        NULL, 
                        CLSCTX_INPROC_SERVER, 
                        IID_ITfThreadMgr, 
                        (void**)&pThreadMgr);

```

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
