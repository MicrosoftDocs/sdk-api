---
UID: NN:msctf.ITfContext
title: ITfContext (msctf.h)
description: The ITfContext interface is implemented by the TSF manager and used by applications and text services to access an edit context.
helpviewer_keywords: ["ITfContext","ITfContext interface [Text Services Framework]","ITfContext interface [Text Services Framework]","described","_tsf_itfcontext_ref","msctf/ITfContext","tsf.itfcontext"]
old-location: tsf\itfcontext.htm
tech.root: TSF
ms.assetid: ca98c7bb-7348-405d-976a-18012b0886c6
ms.date: 12/05/2018
ms.keywords: ITfContext, ITfContext interface [Text Services Framework], ITfContext interface [Text Services Framework],described, _tsf_itfcontext_ref, msctf/ITfContext, tsf.itfcontext
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContext
 - msctf/ITfContext
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
 - ITfContext
---

# ITfContext interface


## -description

The <b>ITfContext</b> interface is implemented by the TSF manager and used by applications and text services to access an edit context.

## -inheritance

The <b>ITfContext</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContext</b> also has these types of members:

## -remarks

An edit context object is created by calling <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a>. Often, a text service uses the currently active edit context. The currently active edit context is the edit context at the top of the stack of the active document manager.


#### Examples


```cpp

HRESULT         hr;
ITfDocumentMgr  *pFocusDoc;

hr = pThreadMgr->GetFocus(&pFocusDoc);
if(SUCCEEDED(hr))
{
    ITfContext *pContext;

    hr = pFocusDoc->GetTop(&pContext);
    if(SUCCEEDED(hr))
    {
        //Use the context. 
        
        pContext->Release();
    }

    pFocusDoc->Release();
}

```

## -see-also

<a href="/windows/desktop/TSF/edit-contexts">Edit Contexts</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
