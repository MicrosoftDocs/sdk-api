---
UID: NF:vidcap.IKsTopologyInfo.get_NumConnections
title: IKsTopologyInfo::get_NumConnections
author: windows-sdk-content
description: The get_NumConnections method returns the number of node connections within the filter.
old-location: dshow\ikstopologyinfo_get_numconnections.htm
old-project: DirectShow
ms.assetid: 55f52b02-2768-4c59-9275-96e238ccf3f0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_NumConnections method, IKsTopologyInfo.get_NumConnections, IKsTopologyInfo::get_NumConnections, IKsTopologyInfoget_NumConnections, dshow.ikstopologyinfo_get_numconnections, get_NumConnections, get_NumConnections method [DirectShow], get_NumConnections method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_NumConnections
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vidcap.h
req.include-header: 
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
 - IKsTopologyInfo.get_NumConnections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IKsTopologyInfo::get_NumConnections


## -description


The <code>get_NumConnections</code> method returns the number of node connections within the filter.


## -parameters




### -param pdwNumConnections [out]

Receives the number of connections.


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
 




## -remarks



To get information about the connections, call the <a href="https://msdn.microsoft.com/ef062e0f-0866-48ca-bd27-26000cd4983a">IKsTopologyInfo::get_ConnectionInfo</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo Interface</a>
 

 

