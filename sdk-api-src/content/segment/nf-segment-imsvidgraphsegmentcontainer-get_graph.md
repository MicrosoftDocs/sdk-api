---
UID: NF:segment.IMSVidGraphSegmentContainer.get_Graph
title: IMSVidGraphSegmentContainer::get_Graph (segment.h)
author: windows-sdk-content
description: The get_Graph method returns a pointer to the Filter Graph Manager.
old-location: mstv\imsvidgraphsegmentcontainer_get_graph.htm
tech.root: mstv
ms.assetid: fecc2953-84d6-4d1b-bb3f-5b966debef1e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidGraphSegmentContainer interface [Microsoft TV Technologies],get_Graph method, IMSVidGraphSegmentContainer.get_Graph, IMSVidGraphSegmentContainer::get_Graph, IMSVidGraphSegmentContainerget_Graph, get_Graph, get_Graph method [Microsoft TV Technologies], get_Graph method [Microsoft TV Technologies],IMSVidGraphSegmentContainer interface, mstv.imsvidgraphsegmentcontainer_get_graph, segment/IMSVidGraphSegmentContainer::get_Graph
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidGraphSegmentContainer.get_Graph
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidGraphSegmentContainer::get_Graph


## -description


The <b>get_Graph</b> method returns a pointer to the Filter Graph Manager.


## -parameters




### -param ppGraph [in]

Address of a variable that receives an <a href="https://msdn.microsoft.com/en-us/library/Dd390085(v=VS.85).aspx">IGraphBuilder</a> interface pointer.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> error code otherwise.




## -remarks



Objects can use this method to find a specific DirectShow filter in the filter graph. It is not recommended that applications use this method. Applications should always control the filter graph using the Video Control.

The returned <a href="https://msdn.microsoft.com/en-us/library/Dd390085(v=VS.85).aspx">IGraphBuilder</a> interface has an outstanding reference count. The caller must release the interface.


#### Examples


```cpp

CComQIPtr<IMSVidGraphSegmentContainer> pSeg(m_pVideoControl);
if (pSeg)
{
    CComPtr<IGraphBuilder> pGraph;
    hr = pSeg->get_Graph(&pGraph);
    if (SUCCEEDED(hr))
    {
        // Use IGraphBuilder::EnumFilters to enumerate the filters.
    }
}

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694566(v=VS.85).aspx">IMSVidGraphSegmentContainer Interface</a>
 

 

