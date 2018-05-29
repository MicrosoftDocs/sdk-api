---
UID: NF:mfidl.IMFTopology.GetSourceNodeCollection
title: IMFTopology::GetSourceNodeCollection
author: windows-sdk-content
description: Gets the source nodes in the topology.
old-location: mf\imftopology_getsourcenodecollection.htm
old-project: medfound
ms.assetid: 9da7d4cd-ad83-4d64-9773-699f39625056
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 9da7d4cd-ad83-4d64-9773-699f39625056, GetSourceNodeCollection, GetSourceNodeCollection method [Media Foundation], GetSourceNodeCollection method [Media Foundation],IMFTopology interface, IMFTopology interface [Media Foundation],GetSourceNodeCollection method, IMFTopology.GetSourceNodeCollection, IMFTopology::GetSourceNodeCollection, mf.imftopology_getsourcenodecollection, mfidl/IMFTopology::GetSourceNodeCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTopology.GetSourceNodeCollection
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopology::GetSourceNodeCollection


## -description



          Gets the source nodes in the topology.
        


## -parameters




### -param ppCollection [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> interface. The caller must release the pointer. The collection contains <b>IUnknown</b> pointers to all of the source nodes in the topology. Each pointer can be queried for the <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface. The collection might be empty.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a>



<a href="https://msdn.microsoft.com/64b2d2b4-1f00-412d-8188-fa361dc317a1">IMFTopologyNode::GetNodeType</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

