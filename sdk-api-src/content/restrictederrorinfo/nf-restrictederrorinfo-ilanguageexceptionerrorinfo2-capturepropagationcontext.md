---
UID: NF:restrictederrorinfo.ILanguageExceptionErrorInfo2.CapturePropagationContext
title: ILanguageExceptionErrorInfo2::CapturePropagationContext (restrictederrorinfo.h)
description: Captures the context of an exception across a language boundary and across threads.
helpviewer_keywords: ["CapturePropagationContext","CapturePropagationContext method [Windows Runtime]","CapturePropagationContext method [Windows Runtime]","ILanguageExceptionErrorInfo2 interface","ILanguageExceptionErrorInfo2 interface [Windows Runtime]","CapturePropagationContext method","ILanguageExceptionErrorInfo2.CapturePropagationContext","ILanguageExceptionErrorInfo2::CapturePropagationContext","restrictederrorinfo/ILanguageExceptionErrorInfo2::CapturePropagationContext","winrt.ilanguageexceptionerrorinfo2_capturepropagationcontext"]
old-location: winrt\ilanguageexceptionerrorinfo2_capturepropagationcontext.htm
tech.root: WinRT
ms.assetid: 60026962-4E6C-4906-97D9-46BD2BCA3AC6
ms.date: 12/05/2018
ms.keywords: CapturePropagationContext, CapturePropagationContext method [Windows Runtime], CapturePropagationContext method [Windows Runtime],ILanguageExceptionErrorInfo2 interface, ILanguageExceptionErrorInfo2 interface [Windows Runtime],CapturePropagationContext method, ILanguageExceptionErrorInfo2.CapturePropagationContext, ILanguageExceptionErrorInfo2::CapturePropagationContext, restrictederrorinfo/ILanguageExceptionErrorInfo2::CapturePropagationContext, winrt.ilanguageexceptionerrorinfo2_capturepropagationcontext
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
 - ILanguageExceptionErrorInfo2::CapturePropagationContext
 - restrictederrorinfo/ILanguageExceptionErrorInfo2::CapturePropagationContext
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
 - ILanguageExceptionErrorInfo2.CapturePropagationContext
---

# ILanguageExceptionErrorInfo2::CapturePropagationContext


## -description

Captures the context of an exception across a language boundary and across threads.

## -parameters

### -param languageException [in]

An error object that's apartment-agile, in-proc, and marshal-by-value across processes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>CapturePropagationContext</b> is utilized by a language projection at re-throw of an error. This includes when an error is received at a language boundary. As such, utilizing <b>CapturePropagationContext</b> helps ensure that the back trace for an exception is captured for a current re-throw. This is to also help ensure that relevant debugging information is not lost when an exception crosses a language border.

Generally speaking, the method creates a linked list of <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> objects that provide additional error information regarding how the exception propagated. This information is exposed as stowed exceptions referenced by the exception record during crash dump analysis. Using this linked list, you can observe the back trace for all language boundaries and threads that the exception propagated through, including where the error originated from.  



#### Examples

The following example demonstrates the projection receiving an error at its language boundary from another projection or  WRL. This is an existing scenario, but allows the system to capture additional context if the previous projection was unable to do so.


```cpp
HRESULT CreateFooExceptionFromLanguageBoundaryError(HRESULT errorReceived, IFooException** createdException)
{
    HRESULT hr = S_OK;
    ComPtr<IFooException> exception;
    // Get the current error
    ComPtr<IRestrictedErrorInfo> restrictedErrorInfo;
    *createdException = nullptr;
    if (SUCCEEDED(GetRestrictedErrorInfo(&restrictedErrorInfo)))
    {
        // Retrieve details regarding the error to determine if it is a stale error
        // or if it is the error we received at the boundary.
        BSTR description;
        HRESULT errorOriginated;
        BSTR restrictedDescription;
        BSTR capabilitySid;
        hr = restrictedErrorInfo->GetErrorDetails(
            &description,
            &errorOriginated,
            &restrictedDescription,
            &capabilitySid);
        if (SUCCEEDED(hr) && errorReceived == errorOriginated)
        {
            hr = CreateFooException(
                errorOriginated,
                restrictedDescription,
                restrictedErrorInfo.Get(),
                &exception);
            // Query for new interface to see if the new logic is there to
            // capture the current propagation context.
            ComPtr<ILanguageExceptionErrorInfo2> languageExceptionErrorInfo;
            if (SUCCEEDED(restrictedErrorInfo.As(&languageExceptionErrorInfo)))
            {
                languageExceptionErrorInfo->CapturePropagationContext(nullptr);
            }		
            *createdException = exception.Detach();
            SetRestrictedErrorInfo(restrictedErrorInfo.Get());
            SysFreeString(description);
            SysFreeString(restrictedDescription);
            SysFreeString(capabilitySid);
            return hr;
        }
        SysFreeString(description);
        SysFreeString(restrictedDescription);
        SysFreeString(capabilitySid);
    }

    // We are here if the error didn't match or we couldn't get error details.
    // So originate a new error.
    // OriginateErrorInfoForThrow will call RoOriginateLanguageException, which will      
    // capture the context
    hr = CreateFooException(errorReceived, nullptr, nullptr, &exception);
    if(SUCCEEDED(hr))
    {
        exception->OriginateErrorInfoForThrow();
        *createdException = exception.Detach();
    }
    return hr;
}


```

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2">ILanguageExceptionErrorInfo2</a>