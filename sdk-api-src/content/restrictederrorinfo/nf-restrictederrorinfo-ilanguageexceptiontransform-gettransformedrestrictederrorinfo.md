---
UID: NF:restrictederrorinfo.ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo
title: ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo (restrictederrorinfo.h)
description: Retrieves the transformed restricted error info.
helpviewer_keywords: ["GetTransformedRestrictedErrorInfo","GetTransformedRestrictedErrorInfo method [Windows Runtime]","GetTransformedRestrictedErrorInfo method [Windows Runtime]","ILanguageExceptionTransform interface","ILanguageExceptionTransform interface [Windows Runtime]","GetTransformedRestrictedErrorInfo method","ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo","ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo","restrictederrorinfo/ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo","winrt.ilanguageexceptiontransform_gettransformedrestrictederrorinfo"]
old-location: winrt\ilanguageexceptiontransform_gettransformedrestrictederrorinfo.htm
tech.root: WinRT
ms.assetid: F64449FE-9562-4210-8C00-9935DE71DA07
ms.date: 12/05/2018
ms.keywords: GetTransformedRestrictedErrorInfo, GetTransformedRestrictedErrorInfo method [Windows Runtime], GetTransformedRestrictedErrorInfo method [Windows Runtime],ILanguageExceptionTransform interface, ILanguageExceptionTransform interface [Windows Runtime],GetTransformedRestrictedErrorInfo method, ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo, ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo, restrictederrorinfo/ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo, winrt.ilanguageexceptiontransform_gettransformedrestrictederrorinfo
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
 - ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo
 - restrictederrorinfo/ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo
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
 - ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo
---

# ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo


## -description

Retrieves the transformed restricted error info.

## -parameters

### -param restrictedErrorInfo [out]

A pointer to an <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> object that contains the restricted error info.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>GetTransformedRestrictedErrorInfo</b> is generally implemented by a language projection in order to expose to the system any and all context from an exception. Specifically, to expose the information from an exception that was thrown from the context of a catch handler that catches a different exception. The thrown exception is considered to be a “transformation” of the caught exception, which is also considered an inner exception by some projections. This allows a developer to obtain insight into why the original exception, before the transform, occurred.  


When implemented, the system uses the <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> retrieved from a call to <b>GetTransformedRestrictedErrorInfo</b> to create another linked list of <b>IRestrictedErrorInfo</b> objects. These objects are exposed in as stowed exceptions in the crash dumps in sequence with the stowed exceptions for the propagations captured in <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo2-capturepropagationcontext">CapturePropagationContext</a>. As with the other exceptions, you can traverse and access these objects in the transformation list using <a href="/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo2-getpreviouslanguageexceptionerrorinfo">GetPreviousLanguageExceptionErrorInfo</a>.


#### Examples


```cpp
[ 
    uuid(7974CD8B-A9EF-4CC4-9A7D-5793CCE30734), 
    pointer_default(unique), 
    object 
] 
interface IFooExceptionInfo : IUnknown 
{ 
    ... 
    HRESULT SetTranformedException(IFooException* exception); 
} 

class FooExceptionInfo : public Microsoft::WRL::RuntimeClass< 
    Microsoft::WRL::RuntimeClassFlags< 
    Microsoft::WRL::RuntimeClassType::ClassicCom>, 
    IFooExceptionInfo, 
    ILanguageExceptionTransform> 
{ 
    ... 
    ... 
private: 
    HRESULT _hr; 
    Microsoft::WRL::Wrappers::HString _message; 
    ComPtr<IFooException> _transformedException; 
public: 
    HRESULT SetTranformedException(IFooException* exception) 
    { 
        _transformedException = exception; 
        return S_OK; 
    } 

    HRESULT GetTransformedRestrictedErrorInfo(IRestrictedErrorInfo** restrictedErrorInfo) 
    { 
        return _transformedException->GetRestrictedErrorForException( 
                   restrictedErrorInfo); 
    } 
} 
[ 
    uuid(52394734-6600-4835-8E17-60BDEDB14B81), 
    pointer_default(unique), 
    object 
] 
interface IFooException : IUnknown 
{ 
    ... 
    HRESULT GetRestrictedErrorForException(IRestrictedErrorInfo** restrictedErrorInfo); 
    HRESULT GetExceptionInfo(IFooExceptionInfo** exceptionInfo); 
} 

class FooException : public Microsoft::WRL::RuntimeClass< 
    Microsoft::WRL::RuntimeClassFlags< 
    Microsoft::WRL::RuntimeClassType::ClassicCom>, 
    IFooException 
    ...> 
{ 
    ... 
    ... 
private: 
    ComPtr<IFooExceptionInfo> _exceptionInfo; 
    ComPtr<IRestrictedErrorInfo> _restrictedErrorInfo;  
public: 
    HRESULT GetRestrictedErrorForException(IRestrictedErrorInfo** restrictedErrorInfo) 
    { 
        return _restrictedErrorInfo.CopyTo(restrictedErrorInfo); 
    } 

    HRESULT GetExceptionInfo(IFooExceptionInfo** exceptionInfo) 
    { 
        return _exceptionInfo.CopyTo(exceptionInfo); 
    } 
} 
void OriginateErrorInfoForThrowWithCaughtException(IFooException* exception, IFooException* caughtException) 
{ 
    ComPtr<IFooExceptionInfo> exceptionInfo;     if(SUCCEEDED(exception->GetExceptionInfo(&exceptionInfo))) 
    { 
        exceptionInfo->SetTranformedException(caughtException); 
        exception->OriginateErrorInfoForThrow(); 
    } 
} 
```

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform">ILanguageExceptionTransform</a>