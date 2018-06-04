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

# ITfSourceSingle interface


## -description


The <b>ITfSourceSingle</b> interface is implemented by the TSF manager. It is used by applications and text services to install and remove various advise sinks. This interface differs from <a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource</a> in that advise sinks installed with <b>ITfSourceSingle</b> only support one advise sink at a time whereas advise sinks installed with <b>ITfSource</b> support multiple simultaneous advise sinks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfSourceSingle</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfSourceSingle</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">AdviseSingleSink</a>
</td>
<td align="left" width="63%">
Installs an advise sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1689dedb-c168-4a05-b598-517c87d9afbd">UnadviseSingleSink</a>
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
<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">
              ITfThreadMgr
            </a>
</li>
<li>
<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">
              ITfContext
            </a>
</li>
</ul>
For more information about advise sinks that can be installed by each implementation, see <a href="https://msdn.microsoft.com/d9231f36-24c4-4d46-97e7-518f5fcc1ce2">ITfSourceSingle::AdviseSingleSink</a>.


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
ITfSourceSingle *pSourceSingle;

hr = pThreadManager-&gt;QueryInterface(IID_ITfSourceSingle, (LPVOID*)&amp;pSourceSingle);
if(SUCCEEDED(hr))
{
    //Use the ITfSourceSingle interface. 
    
    pSourceSingle-&gt;Release();
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
ITfSourceSingle *pSourceSingle;

hr = pContext-&gt;QueryInterface(IID_ITfSourceSingle, (LPVOID*)&amp;pSourceSingle);
if(SUCCEEDED(hr))
{
    //Use the ITfSourceSingle interface. 
    
    pSourceSingle-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">
        ITfContext
      </a>



<a href="https://msdn.microsoft.com/2ff77f09-1b4c-4115-9bb4-4040097d1f90">ITfSource
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">
        ITfThreadMgr
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

