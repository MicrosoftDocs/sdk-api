---
UID: NN:msctf.ITfSource
title: ITfSource
author: windows-sdk-content
description: The ITfSource interface is implemented by the TSF manager. It is used by applications and text services to install and uninstall advise sinks.
old-location: tsf\itfsource.htm
old-project: TSF
ms.assetid: 2ff77f09-1b4c-4115-9bb4-4040097d1f90
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITfSource, ITfSource interface [Text Services Framework], ITfSource interface [Text Services Framework],described, _tsf_itfsource_ref, msctf/ITfSource, tsf.itfsource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSource
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfSource interface


## -description


The <b>ITfSource</b> interface is implemented by the TSF manager. It is used by applications and text services to install and uninstall advise sinks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSource</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfSource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfSource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">AdviseSink</a>
</td>
<td align="left" width="63%">
Installs an advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5d40c6f-c8ab-4e53-94d0-a6b475ce7a84">UnadviseSink</a>
</td>
<td align="left" width="63%">
Uninstalls an advise sink.

</td>
</tr>
</table> 


## -remarks



The TSF manager has different implementations of <b>ITfSource</b>, depending upon how the <b>ITfSource</b> interface is obtained. The difference in the implementations is the types of advise sinks that can be installed with the interface. The different implementations can be obtained from the following objects.

<ul>
<li>
<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">
              ITfThreadMgr
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">
              ITfContext
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3">
              ITfCompartment
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">
              ITfInputProcessorProfiles
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">
              ITfLangBarItem
            </a>
</li>
</ul>
For more information about advise sinks that can be installed by each implementation, see <a href="https://msdn.microsoft.com/90928e6e-e11e-42ad-9b3e-d974642aca36">ITfSource::AdviseSink</a>.


#### Examples

<b>ITfThreadMgr</b>

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pThreadManager-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
<b>ITfContext</b>

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pContext-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
<b>ITfCompartment</b>

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pCompartmentManager-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
<b>ITfInputProcessorProfiles</b>

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pProfiles-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>
<b>ITfLangBarItem</b>

<div class="code"></div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfSource *pSource;

hr = pLangBarItem-&gt;QueryInterface(IID_ITfSource, (LPVOID*)&amp;pSource);
if(SUCCEEDED(hr))
{
    //Use the ITfSource interface. 
    
    pSource-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>


