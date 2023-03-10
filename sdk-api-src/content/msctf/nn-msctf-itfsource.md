---
UID: NN:msctf.ITfSource
title: ITfSource (msctf.h)
description: The ITfSource interface is implemented by the TSF manager. It is used by applications and text services to install and uninstall advise sinks.
helpviewer_keywords: ["ITfSource","ITfSource interface [Text Services Framework]","ITfSource interface [Text Services Framework]","described","_tsf_itfsource_ref","msctf/ITfSource","tsf.itfsource"]
old-location: tsf\itfsource.htm
tech.root: TSF
ms.assetid: 2ff77f09-1b4c-4115-9bb4-4040097d1f90
ms.date: 12/05/2018
ms.keywords: ITfSource, ITfSource interface [Text Services Framework], ITfSource interface [Text Services Framework],described, _tsf_itfsource_ref, msctf/ITfSource, tsf.itfsource
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
 - ITfSource
 - msctf/ITfSource
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
 - ITfSource
---

# ITfSource interface


## -description

The <b>ITfSource</b> interface is implemented by the TSF manager. It is used by applications and text services to install and uninstall advise sinks.

## -inheritance

The <b>ITfSource</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITfSource</b> also has these types of members:

## -remarks

The TSF manager has different implementations of <b>ITfSource</b>, depending upon how the <b>ITfSource</b> interface is obtained. The difference in the implementations is the types of advise sinks that can be installed with the interface. The different implementations can be obtained from the following objects.

<ul>
<li>
<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr
            </a>
</li>
<li>
<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
            </a>
</li>
<li>
<a href="/windows/desktop/api/msctf/nn-msctf-itfcompartment">ITfCompartment
            </a>
</li>
<li>
<a href="/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles">ITfInputProcessorProfiles
            </a>
</li>
<li>
<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem">ITfLangBarItem
            </a>
</li>
</ul>
For more information about advise sinks that can be installed by each implementation, see <a href="/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink">ITfSource::AdviseSink</a>.


#### Examples

<b>ITfThreadMgr</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSource *pSource;

hr = pThreadManager->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource->Release();
}

```


<b>ITfContext</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSource *pSource;

hr = pContext->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource->Release();
}

```


<b>ITfCompartment</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSource *pSource;

hr = pCompartmentManager->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource->Release();
}

```


<b>ITfInputProcessorProfiles</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSource *pSource;

hr = pProfiles->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource->Release();
}

```


<b>ITfLangBarItem</b>

<div class="code"></div>

```cpp

HRESULT hr;
ITfSource *pSource;

hr = pLangBarItem->QueryInterface(IID_ITfSource, (LPVOID*)&pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource->Release();
}

```
