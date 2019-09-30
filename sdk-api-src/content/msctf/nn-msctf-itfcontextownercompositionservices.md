---
UID: NN:msctf.ITfContextOwnerCompositionServices
title: ITfContextOwnerCompositionServices (msctf.h)
author: windows-sdk-content
description: The ITfContextOwnerCompositionServices interface is implemented by the TSF manager and used by a context owner to manipulate compositions created by a text service.
old-location: tsf\itfcontextownercompositionservices.htm
tech.root: TSF
ms.assetid: 7c84cffe-dec8-4e24-b00a-e536984f2a10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionServices, ITfContextOwnerCompositionServices interface [Text Services Framework], ITfContextOwnerCompositionServices interface [Text Services Framework],described, _tsf_itfcontextownercompositionservices_ref, msctf/ITfContextOwnerCompositionServices, tsf.itfcontextownercompositionservices
ms.topic: interface
f1_keywords: 
 - "msctf/ITfContextOwnerCompositionServices"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerCompositionServices
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextOwnerCompositionServices interface


## -description


The <b>ITfContextOwnerCompositionServices</b> interface is implemented by the TSF manager and used by a context owner to manipulate compositions created by a text service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextOwnerCompositionServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfContextOwnerCompositionServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextOwnerCompositionServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition">TerminateComposition</a>
</td>
<td align="left" width="63%">
Terminates a composition.

</td>
</tr>
</table> 


## -remarks



Normally, an application creates a context and is the context owner. On occasion a text service will create a context. In this case, the text service is the context owner. For more information, see <a href="https://docs.microsoft.com/windows/desktop/TSF/edit-contexts">Edit Contexts</a>.

Obtain this interface by calling <b>ITfContext::QueryInterface</b> with IID_ITfContextOwnerCompositionServices.


#### Examples


<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
          </a>


<div class="code"></div>

```cpp

HRESULT hr;
ITfContextOwnerCompositionServices *pCompServices;

//Get the ITfContextOwnerCompositionServices interface pointer. 
hr = m_pContext->QueryInterface(IID_ITfContextOwnerCompositionServices, (LPVOID*)&pCompServices);
if(SUCCEEDED(hr))
{
    //Use the interface. 

    //Release the interface. 
    pCompServices->Release();
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/edit-contexts">Edit Contexts</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

