---
UID: NN:msctf.ITfQueryEmbedded
title: ITfQueryEmbedded
author: windows-sdk-content
description: The ITfQueryEmbedded interface is implemented by the TSF manager and used by a text service to determine if a context can accept an embedded object.
old-location: tsf\itfqueryembedded.htm
tech.root: TSF
ms.assetid: 6e2c3ad5-73c6-481f-9ade-58782e12dfbd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfQueryEmbedded, ITfQueryEmbedded interface [Text Services Framework], ITfQueryEmbedded interface [Text Services Framework],described, _tsf_itfqueryembedded_ref, msctf/ITfQueryEmbedded, tsf.itfqueryembedded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfQueryEmbedded
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfQueryEmbedded interface


## -description


The <b>ITfQueryEmbedded</b> interface is implemented by the TSF manager and used by a text service to determine if a context can accept an embedded object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfQueryEmbedded</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfQueryEmbedded</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfQueryEmbedded</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52f9465f-725e-493b-89ee-1b3db3cef696">QueryInsertEmbedded</a>
</td>
<td align="left" width="63%">
Determines if the active context can accept an embedded object.

</td>
</tr>
</table> 


## -remarks



To obtain an instance of this interface, call the <b>ITfContext::QueryInterface</b> method with IID_ITfQueryEmbedded.


#### Examples


<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
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




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

