---
UID: NN:restrictederrorinfo.ILanguageExceptionStackBackTrace
title: ILanguageExceptionStackBackTrace (restrictederrorinfo.h)
description: Allows projections to provide custom stack trace for that exception.
helpviewer_keywords: ["ILanguageExceptionStackBackTrace","ILanguageExceptionStackBackTrace interface [Windows Runtime]","ILanguageExceptionStackBackTrace interface [Windows Runtime]","described","restrictederrorinfo/ILanguageExceptionStackBackTrace","winrt.ilanguageexceptionstackbacktrace"]
old-location: winrt\ilanguageexceptionstackbacktrace.htm
tech.root: WinRT
ms.assetid: A5AA17A2-414B-4641-A417-4F73384216F9
ms.date: 12/05/2018
ms.keywords: ILanguageExceptionStackBackTrace, ILanguageExceptionStackBackTrace interface [Windows Runtime], ILanguageExceptionStackBackTrace interface [Windows Runtime],described, restrictederrorinfo/ILanguageExceptionStackBackTrace, winrt.ilanguageexceptionstackbacktrace
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILanguageExceptionStackBackTrace
 - restrictederrorinfo/ILanguageExceptionStackBackTrace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionStackBackTrace
---

# ILanguageExceptionStackBackTrace interface


## -description

Allows projections to provide custom stack trace for that exception.

## -inheritance

The <b>ILanguageExceptionStackBackTrace</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILanguageExceptionStackBackTrace</b> also has these types of members:

## -remarks

It is recommended that language projections implement this interface when the stack trace is not captured by the relevant Global Error Handler API.


#### Examples

The following example demonstrates a projection providing its back trace through an interface implemented on the language exception object.  Global Error Handling (GEH) queries for this interface when a language exception object is provided to <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception">RoOriginateLanguageException</a> or <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo2-capturepropagationcontext">CapturePropagationContext</a>.  As such, this scenario allows the GEH to expose back traces for projections which the GEH can’t capture back traces for.


```cpp
class FooExceptionInfo : public Microsoft::WRL::RuntimeClass< 
    Microsoft::WRL::RuntimeClassFlags< 
    Microsoft::WRL::RuntimeClassType::ClassicCom>, 
    ... 
    ILanguageExceptionStackBackTrace > 
{ 
    ... 
    ... 
private: 
    UINT_PTR* customBackTrace; 
    int numFramesCaptured; 
public: 
    HRESULT GetStackBackTrace( 
        ULONG maxFramesToCapture, 
        UINT_PTR stackBackTrace [], 
        ULONG* framesCaptured) 
    { 
        int idx = 0; 
        for (; idx < maxFramesToCapture && idx < numFramesCaptured; idx++) 
        { 
            stackBackTrace[idx] = customBackTrace[idx]; 
        } 
        *framesCaptured = idx; 
        return S_OK; 
    } 
} 

```

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
