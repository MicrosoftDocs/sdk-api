---
UID: NN:inputscope.ITfInputScope
title: ITfInputScope (inputscope.h)
description: The ITfInputScope interface is used by the text input processors to get the InputScope value that represents a document context associated with a window.
helpviewer_keywords: ["ITfInputScope","ITfInputScope interface [Text Services Framework]","ITfInputScope interface [Text Services Framework]","described","_tsf_itfinputscope_ref","inputscope/ITfInputScope","tsf.ITfInputScope"]
old-location: tsf\ITfInputScope.htm
tech.root: TSF
ms.assetid: b2a045dd-dc2c-489d-bcb9-80710faef9c2
ms.date: 12/05/2018
ms.keywords: ITfInputScope, ITfInputScope interface [Text Services Framework], ITfInputScope interface [Text Services Framework],described, _tsf_itfinputscope_ref, inputscope/ITfInputScope, tsf.ITfInputScope
req.header: inputscope.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputScope.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputScope
 - inputscope/ITfInputScope
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
 - ITfInputScope
---

# ITfInputScope interface


## -description

The <b>ITfInputScope</b> interface is used by the text input processors to get the <a href="/windows/win32/api/inputscope/ne-inputscope-inputscope">InputScope</a> value that represents a document context associated with a window. The input scope provides rules to help speech and handwriting recognition. For instance, if a text box on a form is used to enter an address, the input scope for that text box can be set to recognize and accept only those characters that are valid for an address.

The interface ID is IID_ITfInputScope.

The document context is used by the speech and handwriting recognition engine and is set by a text input processor by calling the <a href="/windows/desktop/api/inputscope/nf-inputscope-setinputscope">SetInputScope</a> method. A TSF-aware application does not call <b>SetInputScope</b> directly, but rather implements either <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> or <a href="/windows/desktop/api/msctf/nn-msctf-itfcontextowner">ITfContextOwner</a> to get a pointer to <b>ITfInputScope</b>.

To get the pointer to the <b>ITfInputScope</b> interface, the text input processor or TSF-aware application calls <a href="/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty">ITfContext::GetAppProperty</a>, passing in <b>GUID_PROP_INPUTSCOPE</b> and a pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITFReadOnlyProperty</a> interface, as in the following example.

```cpp

extern const GUID GUID_PROP_INPUTSCOPE;
// 
// The TIP can call this to get the input scope of the document mgr. 
// 
HRESULT GetInputScope(ITfContext *pic, ITfRange *pRange, TfEditCookie ec, ITfInutScope **ppiscope){
    ITFReadOnlyProperty *prop;
    HRESULT hr;
    If (SUCCEEDED(hr = pic->GetAppProperty(GUID_PROP_INPUTSCOPE, &prop))
    {   VARIANT var;
        If (SUCCEEDED(hr = prop->GetValue(ec, pRange, &var)))
        {  hr = var.punkVal->QueryInterface(IID_ITfInputScope, (void **)ppiscope);
        }
        prop->Release();
    }
    return hr
}

```

## -inheritance

The <b>ITfInputScope</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfInputScope</b> also has these types of members:

## -remarks

To use this interface with window-less controls, an application has two options.

<ol>
<li><b>Make the application TSF-aware:  </b>A TSF-aware application must implement either <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> or <a href="/windows/desktop/api/msctf/nn-msctf-itfcontextowner">ITfContextOwner</a> to get a pointer to <b>ITfInputScope</b>.</li>
<li>
<a href="/windows/desktop/api/inputscope/nf-inputscope-setinputscopes">SetInputScopes</a>  This is not recommended, but if the application is not TSF-aware, there is no other way to maintain the association between the input scope and the application. In this case, the application must call SetInputScopes whenever focus changes among window-less controls.</li>
</ol>
