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

# IMSVidGraphSegmentContainer::get_Graph


## -description


The <b>get_Graph</b> method returns a pointer to the Filter Graph Manager.


## -parameters




### -param ppGraph [in]

Address of a variable that receives an <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface pointer.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -remarks



Objects can use this method to find a specific DirectShow filter in the filter graph. It is not recommended that applications use this method. Applications should always control the filter graph using the Video Control.

The returned <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface has an outstanding reference count. The caller must release the interface.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComQIPtr&lt;IMSVidGraphSegmentContainer&gt; pSeg(m_pVideoControl);
if (pSeg)
{
    CComPtr&lt;IGraphBuilder&gt; pGraph;
    hr = pSeg-&gt;get_Graph(&amp;pGraph);
    if (SUCCEEDED(hr))
    {
        // Use IGraphBuilder::EnumFilters to enumerate the filters.
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a314693f-8fc2-4816-b64b-d5f8886da39e">IMSVidGraphSegmentContainer Interface</a>
 

 

