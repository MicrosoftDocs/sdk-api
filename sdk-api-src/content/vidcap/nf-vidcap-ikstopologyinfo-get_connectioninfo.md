---
UID: NF:vidcap.IKsTopologyInfo.get_ConnectionInfo
title: IKsTopologyInfo::get_ConnectionInfo
author: windows-sdk-content
description: The get_ConnectionInfo method returns information about one node connection in the filter.
old-location: dshow\ikstopologyinfo_get_connectioninfo.htm
tech.root: DirectShow
ms.assetid: ef062e0f-0866-48ca-bd27-26000cd4983a
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IKsTopologyInfo interface [DirectShow],get_ConnectionInfo method, IKsTopologyInfo.get_ConnectionInfo, IKsTopologyInfo::get_ConnectionInfo, IKsTopologyInfoget_ConnectionInfo, dshow.ikstopologyinfo_get_connectioninfo, get_ConnectionInfo, get_ConnectionInfo method [DirectShow], get_ConnectionInfo method [DirectShow],IKsTopologyInfo interface, vidcap/IKsTopologyInfo::get_ConnectionInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IKsTopologyInfo.get_ConnectionInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsTopologyInfo::get_ConnectionInfo


## -description


The <code>get_ConnectionInfo</code> method returns information about one node connection in the filter.


## -parameters




### -param dwIndex [in]

Index of the connection. To find the number of connections, call the <a href="https://msdn.microsoft.com/55f52b02-2768-4c59-9275-96e238ccf3f0">IKsTopologyInfo::get_NumConnections</a> method.


### -param pConnectionInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/8fca47b7-4c52-46db-809c-77a0e3414276">KSTOPOLOGY_CONNECTION</a> structure allocated by the caller. The method fills in this structure with the connection information.


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
 

 

