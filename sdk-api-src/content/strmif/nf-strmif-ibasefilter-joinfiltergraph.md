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

# IBaseFilter::JoinFilterGraph


## -description



The <code>JoinFilterGraph</code> method notifies the filter that it has joined or left the filter graph.




## -parameters




### -param pGraph [in]

Pointer to the Filter Graph Manager's <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> interface, or <b>NULL</b> if the filter is leaving the graph.


### -param pName [in]

Pointer to a wide-character string that specifies a name for the filter.


## -returns



Returns S_OK if successful, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



When the Filter Graph Manager adds a filter to the filter graph, it calls this method with a pointer to itself. It assigns a name for this instance of the filter through the <i>pName</i> parameter. The name can be retrieved by calling the <a href="https://msdn.microsoft.com/6cb9b6ef-05ae-4816-b337-dd90cab843fb">IBaseFilter::QueryFilterInfo</a> method.

When the Filter Graph Manager removes the filter from the graph, it calls this method with a <b>NULL</b> pointer.

Applications should never call this method. To add a filter to the graph, call the <a href="https://msdn.microsoft.com/8f837917-015f-427f-b234-b0ccbcf943eb">IFilterGraph::AddFilter</a> method on the filter graph manager.

<b>Filter developers</b>: The filter can store the <b>IFilterGraph</b> interface pointer and query it for other Filter Graph Manager interfaces. However, it must never hold a reference count on the Filter Graph Manager. Doing so creates a circular reference count, because the Filter Graph Manager keeps a reference count on the filter. A circular reference count prevents the interface from being released properly, which can lead to a deadlock. The <b>IFilterGraph</b> interface is guaranteed to be valid until the Filter Graph Manager calls this method again with the value <b>NULL</b>. For an implementation of this method, see the <a href="https://msdn.microsoft.com/ee02650c-aaf0-4a0e-914f-180230010709">CBaseFilter::JoinFilterGraph</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter Interface</a>
 

 

