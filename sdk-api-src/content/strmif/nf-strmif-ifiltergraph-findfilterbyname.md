---
UID: NF:strmif.IFilterGraph.FindFilterByName
title: IFilterGraph::FindFilterByName
author: windows-sdk-content
description: The FindFilterByName method finds a filter that was added to the filter graph with a specific name.
old-location: dshow\ifiltergraph_findfilterbyname.htm
old-project: DirectShow
ms.assetid: 59d90274-ac00-4e19-bcee-2282e26994b5
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: FindFilterByName, FindFilterByName method [DirectShow], FindFilterByName method [DirectShow],IFilterGraph interface, IFilterGraph interface [DirectShow],FindFilterByName method, IFilterGraph.FindFilterByName, IFilterGraph::FindFilterByName, IFilterGraphFindFilterByName, dshow.ifiltergraph_findfilterbyname, strmif/IFilterGraph::FindFilterByName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterGraph.FindFilterByName
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IFilterGraph::FindFilterByName


## -description



The <code>FindFilterByName</code> method finds a filter that was added to the filter graph with a specific name.




## -parameters




### -param pName [in]

[in, string] Pointer to the name to search for.


### -param ppFilter [out]

Receives a pointer to the filter's <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface. The caller must release the interface.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No filter was found with the specified name.

</td>
</tr>
</table>
 




## -remarks



If no filter is found, the method returns a <b>NULL</b> pointer in the <i>ppFilter</i> parameter.

The returned <b>IBaseFilter</b> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph Interface</a>
 

 

