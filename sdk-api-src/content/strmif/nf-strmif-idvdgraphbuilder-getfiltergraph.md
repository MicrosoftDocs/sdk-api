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

# IDvdGraphBuilder::GetFiltergraph


## -description



The <code>GetFiltergraph</code> method retrieves the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface for the filter graph used by the DVD-Video graph builder object.




## -parameters




### -param ppGB [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface that the DVD-Video graph builder object is using.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The current DirectShow implementation returns E_INVALIDARG if <i>ppGB</i> is invalid.




## -remarks



The returned <b>IGraphBuilder</b> interface pointer has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2179e54a-c6e2-4837-9f89-be210bde9180">IDvdGraphBuilder Interface</a>
 

 

