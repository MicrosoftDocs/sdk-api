---
UID: NN:msctf.ITfQueryEmbedded
title: ITfQueryEmbedded (msctf.h)
description: The ITfQueryEmbedded interface is implemented by the TSF manager and used by a text service to determine if a context can accept an embedded object.
helpviewer_keywords: ["ITfQueryEmbedded","ITfQueryEmbedded interface [Text Services Framework]","ITfQueryEmbedded interface [Text Services Framework]","described","_tsf_itfqueryembedded_ref","msctf/ITfQueryEmbedded","tsf.itfqueryembedded"]
old-location: tsf\itfqueryembedded.htm
tech.root: TSF
ms.assetid: 6e2c3ad5-73c6-481f-9ade-58782e12dfbd
ms.date: 12/05/2018
ms.keywords: ITfQueryEmbedded, ITfQueryEmbedded interface [Text Services Framework], ITfQueryEmbedded interface [Text Services Framework],described, _tsf_itfqueryembedded_ref, msctf/ITfQueryEmbedded, tsf.itfqueryembedded
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfQueryEmbedded
 - msctf/ITfQueryEmbedded
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
 - ITfQueryEmbedded
---

# ITfQueryEmbedded interface


## -description

The <b>ITfQueryEmbedded</b> interface is implemented by the TSF manager and used by a text service to determine if a context can accept an embedded object.

## -inheritance

The <b>ITfQueryEmbedded</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfQueryEmbedded</b> also has these types of members:

## -remarks

To obtain an instance of this interface, call the <b>ITfContext::QueryInterface</b> method with IID_ITfQueryEmbedded.


#### Examples


<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
          </a>


<div class="code"></div>

```cpp

HRESULT hr;
ITfQueryEmbedded *pQueryEmbedded;

hr = pContext->QueryInterface(IID_ITfQueryEmbedded, (LPVOID*)&pQueryEmbedded);
if(SUCCEEDED(hr))
{
    //Use the ITfQueryEmbedded interface. 
    
    pQueryEmbedded->Release();
}

```

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
