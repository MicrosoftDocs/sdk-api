---
UID: NF:msctf.ITfTextLayoutSink.OnLayoutChange
title: ITfTextLayoutSink::OnLayoutChange (msctf.h)
description: ITfTextLayoutSink::OnLayoutChange method
helpviewer_keywords: ["ITfTextLayoutSink interface [Text Services Framework]","OnLayoutChange method","ITfTextLayoutSink.OnLayoutChange","ITfTextLayoutSink::OnLayoutChange","OnLayoutChange","OnLayoutChange method [Text Services Framework]","OnLayoutChange method [Text Services Framework]","ITfTextLayoutSink interface","_tsf_itftextlayoutsink_onlayoutchange_ref","msctf/ITfTextLayoutSink::OnLayoutChange","tsf.itftextlayoutsink_onlayoutchange"]
old-location: tsf\itftextlayoutsink_onlayoutchange.htm
tech.root: TSF
ms.assetid: a99313ab-98a7-4fc0-b3ae-78ff26a41d8e
ms.date: 12/05/2018
ms.keywords: ITfTextLayoutSink interface [Text Services Framework],OnLayoutChange method, ITfTextLayoutSink.OnLayoutChange, ITfTextLayoutSink::OnLayoutChange, OnLayoutChange, OnLayoutChange method [Text Services Framework], OnLayoutChange method [Text Services Framework],ITfTextLayoutSink interface, _tsf_itftextlayoutsink_onlayoutchange_ref, msctf/ITfTextLayoutSink::OnLayoutChange, tsf.itftextlayoutsink_onlayoutchange
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfTextLayoutSink::OnLayoutChange
 - msctf/ITfTextLayoutSink::OnLayoutChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - ITfTextLayoutSink.OnLayoutChange
---

# ITfTextLayoutSink::OnLayoutChange


## -description

Receives a notification when the layout of a context view changes.

## -parameters

### -param pic [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface for the context that changed.

### -param lcode [in]

Specifies the <a href="/windows/win32/api/msctf/ne-msctf-tflayoutcode">TfLayoutCode</a> element that describes the layout change.

### -param pView [in]

Pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView</a> interface for the context view in that the layout change occurred.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each context has a default view for which a reference can be obtained using the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getactiveview">ITfContext::GetActiveView</a> method. The method returns only the value TF_LC_CHANGE for the <i>lcode</i> parameter for this view, because the values are possible only for multiple views. Because TSF does not support multiple views, this method never receives other values of the <b>TfLayoutCode</b> enumeration.

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getactiveview">ITfContext::GetActiveView
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextview">ITfContextView
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itftextlayoutsink">ITfTextLayoutSink
      </a>



<a href="/windows/win32/api/msctf/ne-msctf-tflayoutcode">TfLayoutCode
      </a>