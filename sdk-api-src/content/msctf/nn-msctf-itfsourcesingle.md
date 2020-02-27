---
UID: NN:msctf.ITfSourceSingle
title: ITfSourceSingle (msctf.h)
description: The ITfSourceSingle interface is implemented by the TSF manager.
old-location: tsf\itfsourcesingle.htm
tech.root: TSF
ms.assetid: 01e60ede-b871-4b38-b2ee-24f79c5b3e80
ms.date: 12/05/2018
ms.keywords: ITfSourceSingle, ITfSourceSingle interface [Text Services Framework], ITfSourceSingle interface [Text Services Framework],described, _tsf_itfsourcesingle_ref, msctf/ITfSourceSingle, tsf.itfsourcesingle
f1_keywords:
- msctf/ITfSourceSingle
dev_langs:
- c++
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
- ITfSourceSingle
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfSourceSingle interface


## -description


The <b>ITfSourceSingle</b> interface is implemented by the TSF manager. It is used by applications and text services to install and remove various advise sinks. This interface differs from <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource</a> in that advise sinks installed with <b>ITfSourceSingle</b> only support one advise sink at a time whereas advise sinks installed with <b>ITfSource</b> support multiple simultaneous advise sinks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSourceSingle</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSourceSingle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfSourceSingle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">AdviseSingleSink</a>
</td>
<td align="left" width="63%">
Installs an advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-unadvisesinglesink">UnadviseSingleSink</a>
</td>
<td align="left" width="63%">
Uninstalls an advise sink.

</td>
</tr>
</table> 


## -remarks



The TSF manager has different implementations of <b>ITfSourceSingle</b>, depending upon how the <b>ITfSourceSingle</b> interface is obtained. The difference in the implementations is the types of advise sinks that can be installed with the interface. The different implementations can be obtained from the following objects.

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
            </a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
            </a>
</li>
</ul>
For more information about advise sinks that can be installed by each implementation, see <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfsourcesingle-advisesinglesink">ITfSourceSingle::AdviseSingleSink</a>.


#### Examples

<b>ITfThreadMgr</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSourceSingle *pSourceSingle;

hr = pThreadManager->QueryInterface(IID_ITfSourceSingle, (LPVOID*)&pSourceSingle);
if(SUCCEEDED(hr))
{
    //Use the ITfSourceSingle interface. 
    
    pSourceSingle->Release();
}

```


<b>ITfContext</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSourceSingle *pSourceSingle;

hr = pContext->QueryInterface(IID_ITfSourceSingle, (LPVOID*)&pSourceSingle);
if(SUCCEEDED(hr))
{
    //Use the ITfSourceSingle interface. 
    
    pSourceSingle->Release();
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfsource">ITfSource
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

