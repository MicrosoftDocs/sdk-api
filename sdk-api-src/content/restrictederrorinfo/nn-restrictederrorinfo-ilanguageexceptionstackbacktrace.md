---
UID: NN:restrictederrorinfo.ILanguageExceptionStackBackTrace
title: ILanguageExceptionStackBackTrace
author: windows-sdk-content
description: Allows projections to provide custom stack trace for that exception.
old-location: winrt\ilanguageexceptionstackbacktrace.htm
tech.root: WinRT
ms.assetid: A5AA17A2-414B-4641-A417-4F73384216F9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ILanguageExceptionStackBackTrace, ILanguageExceptionStackBackTrace interface [Windows Runtime], ILanguageExceptionStackBackTrace interface [Windows Runtime],described, restrictederrorinfo/ILanguageExceptionStackBackTrace, winrt.ilanguageexceptionstackbacktrace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ILanguageExceptionStackBackTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILanguageExceptionStackBackTrace interface


## -description


Allows projections to provide custom stack trace for that exception. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageExceptionStackBackTrace</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILanguageExceptionStackBackTrace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageExceptionStackBackTrace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EB89F76-C518-41A3-A1F8-EC480B0FC68B">GetStackBackTrace</a>
</td>
<td align="left" width="63%">
Retrieves the back stack trace.

</td>
</tr>
</table> 


## -remarks



It is recommended that language projections implement this interface when the stack trace is not captured by the relevant Global Error Handler API.


#### Examples

The following example demonstrates a projection providing its back trace through an interface implemented on the language exception object.  Global Error Handling (GEH) queries for this interface when a language exception object is provided to <a href="https://msdn.microsoft.com/573A9209-31EF-4FD4-A504-16795BA42337">RoOriginateLanguageException</a> or <a href="https://msdn.microsoft.com/60026962-4E6C-4906-97D9-46BD2BCA3AC6">CapturePropagationContext</a>.  As such, this scenario allows the GEH to expose back traces for projections which the GEH can’t capture back traces for.


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




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

