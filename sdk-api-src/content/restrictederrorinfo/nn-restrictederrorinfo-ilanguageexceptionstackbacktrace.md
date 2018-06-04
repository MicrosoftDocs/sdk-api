---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>class FooExceptionInfo : public Microsoft::WRL::RuntimeClass&lt; 
    Microsoft::WRL::RuntimeClassFlags&lt; 
    Microsoft::WRL::RuntimeClassType::ClassicCom&gt;, 
    ... 
    ILanguageExceptionStackBackTrace &gt; 
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
        for (; idx &lt; maxFramesToCapture &amp;&amp; idx &lt; numFramesCaptured; idx++) 
        { 
            stackBackTrace[idx] = customBackTrace[idx]; 
        } 
        *framesCaptured = idx; 
        return S_OK; 
    } 
} 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

