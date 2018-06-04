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
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT hr;
ITfQueryEmbedded *pQueryEmbedded;

hr = pContext-&gt;QueryInterface(IID_ITfQueryEmbedded, (LPVOID*)&amp;pQueryEmbedded);
if(SUCCEEDED(hr))
{
    //Use the ITfQueryEmbedded interface. 
    
    pQueryEmbedded-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

