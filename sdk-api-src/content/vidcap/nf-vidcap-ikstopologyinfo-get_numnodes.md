---
UID: NF:vidcap.IKsTopologyInfo.get_NumNodes
title: IKsTopologyInfo::get_NumNodes
author: windows-sdk-content
description: The get_NumNodes method returns the number of nodes in the filter.
old-location: dshow\ikstopologyinfo_get_numnodes.htm
old-project: DirectShow
ms.assetid: fdba99d5-fd44-4d4f-8575-867d98bf3339
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NumNodes method, IKsTopologyInfo.get_NumNodes, IKsTopologyInfo::get_NumNodes, IKsTopologyInfoget_NumNodes, dshow.ikstopologyinfo_get_numnodes, get_NumNodes, get_NumNodes method [DirectShow], get_NumNodes method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NumNodes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_NumNodes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IKsTopologyInfo::get_NumNodes


## -description


The <code>get_NumNodes</code> method returns the number of nodes in the filter.


## -parameters




### -param pdwNumNodes [out]

Receives the number of nodes.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo Interface</a>
 

 

