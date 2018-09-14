---
UID: NF:vidcap.IKsTopologyInfo.CreateNodeInstance
title: IKsTopologyInfo::CreateNodeInstance
author: windows-sdk-content
description: The CreateNodeInstance method creates a COM object that represents a node in the filter.
old-location: dshow\ikstopologyinfo_createnodeinstance.htm
tech.root: DirectShow
ms.assetid: f2c7ea1d-abd6-4179-b5b7-d89837ceecd7
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateNodeInstance, CreateNodeInstance method [DirectShow], CreateNodeInstance method [DirectShow],IKsTopologyInfo interface, IKsTopologyInfo interface [DirectShow],CreateNodeInstance method, IKsTopologyInfo.CreateNodeInstance, IKsTopologyInfo::CreateNodeInstance, IKsTopologyInfoCreateNodeInstance, dshow.ikstopologyinfo_createnodeinstance, vidcap/IKsTopologyInfo::CreateNodeInstance
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
 - IKsTopologyInfo.CreateNodeInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IKsTopologyInfo::CreateNodeInstance


## -description


The <code>CreateNodeInstance</code> method creates a COM object that represents a node in the filter.


## -parameters




### -param dwNodeId [in]

Index of the node to create. To find the number of nodes, call the <a href="https://msdn.microsoft.com/fdba99d5-fd44-4d4f-8575-867d98bf3339">IKsTopologyInfo::get_NumNodes</a> method.


### -param iid [in]

Interface identifier (IID) of the interface to return.


### -param ppvObject [out]

Receives a pointer to the requested interface on the node object. The caller must release the interface.


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



Node objects expose the <b>IKsControl</b> interface. You can use this interface to enumerate and access the node's property sets.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/641a10fe-8e8c-4225-b05e-b09dfb5f2fee">IKsTopologyInfo Interface</a>
 

 

