---
UID: NF:restrictederrorinfo.ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo
title: ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo
author: windows-sdk-content
description: Retrieves the transformed restricted error info.
old-location: winrt\ilanguageexceptiontransform_gettransformedrestrictederrorinfo.htm
tech.root: WinRT
ms.assetid: F64449FE-9562-4210-8C00-9935DE71DA07
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTransformedRestrictedErrorInfo, GetTransformedRestrictedErrorInfo method [Windows Runtime], GetTransformedRestrictedErrorInfo method [Windows Runtime],ILanguageExceptionTransform interface, ILanguageExceptionTransform interface [Windows Runtime],GetTransformedRestrictedErrorInfo method, ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo, ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo, restrictederrorinfo/ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo, winrt.ilanguageexceptiontransform_gettransformedrestrictederrorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionTransform.GetTransformedRestrictedErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILanguageExceptionTransform::GetTransformedRestrictedErrorInfo


## -description


Retrieves the transformed restricted error info.


## -parameters




### -param restrictedErrorInfo [out]

A pointer to an <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> object that contains the restricted error info. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>GetTransformedRestrictedErrorInfo</b> is generally implemented by a language projection in order to expose to the system any and all context from an exception. Specifically, to expose the information from an exception that was thrown from the context of a catch handler that catches a different exception. The thrown exception is considered to be a “transformation” of the caught exception, which is also considered an inner exception by some projections. This allows a developer to obtain insight into why the original exception, before the transform, occurred.  


When implemented, the system uses the <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> retrieved from a call to <b>GetTransformedRestrictedErrorInfo</b> to create another linked list of <b>IRestrictedErrorInfo</b> objects. These objects are exposed in as stowed exceptions in the crash dumps in sequence with the stowed exceptions for the propagations captured in <a href="https://msdn.microsoft.com/60026962-4E6C-4906-97D9-46BD2BCA3AC6">CapturePropagationContext</a>. As with the other exceptions, you can traverse and access these objects in the transformation list using <a href="https://msdn.microsoft.com/10A45EF1-AF8F-498D-B95B-FCE9EF8AB203">GetPreviousLanguageExceptionErrorInfo</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>[ 
    uuid(7974CD8B-A9EF-4CC4-9A7D-5793CCE30734), 
    pointer_default(unique), 
    object 
] 
interface IFooExceptionInfo : IUnknown 
{ 
    ... 
    HRESULT SetTranformedException(IFooException* exception); 
} 

class FooExceptionInfo : public Microsoft::WRL::RuntimeClass&lt; 
    Microsoft::WRL::RuntimeClassFlags&lt; 
    Microsoft::WRL::RuntimeClassType::ClassicCom&gt;, 
    IFooExceptionInfo, 
    ILanguageExceptionTransform&gt; 
{ 
    ... 
    ... 
private: 
    HRESULT _hr; 
    Microsoft::WRL::Wrappers::HString _message; 
    ComPtr&lt;IFooException&gt; _transformedException; 
public: 
    HRESULT SetTranformedException(IFooException* exception) 
    { 
        _transformedException = exception; 
        return S_OK; 
    } 

    HRESULT GetTransformedRestrictedErrorInfo(IRestrictedErrorInfo** restrictedErrorInfo) 
    { 
        return _transformedException-&gt;GetRestrictedErrorForException( 
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

class FooException : public Microsoft::WRL::RuntimeClass&lt; 
    Microsoft::WRL::RuntimeClassFlags&lt; 
    Microsoft::WRL::RuntimeClassType::ClassicCom&gt;, 
    IFooException 
    ...&gt; 
{ 
    ... 
    ... 
private: 
    ComPtr&lt;IFooExceptionInfo&gt; _exceptionInfo; 
    ComPtr&lt;IRestrictedErrorInfo&gt; _restrictedErrorInfo;  
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
    ComPtr&lt;IFooExceptionInfo&gt; exceptionInfo;     if(SUCCEEDED(exception-&gt;GetExceptionInfo(&amp;exceptionInfo))) 
    { 
        exceptionInfo-&gt;SetTranformedException(caughtException); 
        exception-&gt;OriginateErrorInfoForThrow(); 
    } 
} </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/A42470EE-FA05-4716-BA17-009D59FEE259">ILanguageExceptionTransform</a>
 

 

