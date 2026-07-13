---
UID: NN:msctf.ITfContextOwnerCompositionServices
title: ITfContextOwnerCompositionServices (msctf.h)
description: The ITfContextOwnerCompositionServices interface is implemented by the TSF manager and used by a context owner to manipulate compositions created by a text service.
helpviewer_keywords: ["ITfContextOwnerCompositionServices","ITfContextOwnerCompositionServices interface [Text Services Framework]","ITfContextOwnerCompositionServices interface [Text Services Framework]","described","_tsf_itfcontextownercompositionservices_ref","msctf/ITfContextOwnerCompositionServices","tsf.itfcontextownercompositionservices"]
old-location: tsf\itfcontextownercompositionservices.htm
tech.root: TSF
ms.assetid: 7c84cffe-dec8-4e24-b00a-e536984f2a10
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionServices, ITfContextOwnerCompositionServices interface [Text Services Framework], ITfContextOwnerCompositionServices interface [Text Services Framework],described, _tsf_itfcontextownercompositionservices_ref, msctf/ITfContextOwnerCompositionServices, tsf.itfcontextownercompositionservices
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
 - ITfContextOwnerCompositionServices
 - msctf/ITfContextOwnerCompositionServices
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
 - ITfContextOwnerCompositionServices
---

# ITfContextOwnerCompositionServices interface


## -description

The <b>ITfContextOwnerCompositionServices</b> interface is implemented by the TSF manager and used by a context owner to manipulate compositions created by a text service.

## -inheritance

The <b>ITfContextOwnerCompositionServices</b> interface inherits from the <a href="/windows/win32/api/msctf/nn-msctf-itfcontextcomposition">ITfContextComposition</a> interface. <b>ITfContextOwnerCompositionServices</b> also has these types of members:

## -remarks

Normally, an application creates a context and is the context owner. On occasion a text service will create a context. In this case, the text service is the context owner. For more information, see <a href="/windows/desktop/TSF/edit-contexts">Edit Contexts</a>.

Obtain this interface by calling <b>ITfContext::QueryInterface</b> with IID_ITfContextOwnerCompositionServices.


#### Examples


<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
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

<a href="/windows/desktop/TSF/edit-contexts">Edit Contexts</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/win32/api/msctf/nn-msctf-itfcontextcomposition">ITfContextComposition</a>
