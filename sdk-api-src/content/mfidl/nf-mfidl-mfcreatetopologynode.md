---
UID: NF:mfidl.MFCreateTopologyNode
title: MFCreateTopologyNode function
author: windows-sdk-content
description: Creates a topology node.
old-location: mf\mfcreatetopologynode.htm
tech.root: medfound
ms.assetid: 67c32232-09cb-4098-b80b-4b93ee121190
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: 67c32232-09cb-4098-b80b-4b93ee121190, MFCreateTopologyNode, MFCreateTopologyNode function [Media Foundation], mf.mfcreatetopologynode, mfidl/MFCreateTopologyNode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateTopologyNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateTopologyNode function


## -description


Creates a topology node.


## -parameters




### -param NodeType [in]

The type of node to create, specified as a member of the <a href="https://msdn.microsoft.com/73ea1f48-0d86-4104-860c-83a4f9189920">MF_TOPOLOGY_TYPE</a> enumeration.


### -param ppNode [out]

Receives a pointer to the node's <a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a> interface. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e548f2a-77cd-460e-9ffd-c098f6ee75eb">Creating Output Nodes</a>



<a href="https://msdn.microsoft.com/44c26bcd-04a9-48c3-b536-25c2b18c34c1">Creating Source Nodes</a>



<a href="https://msdn.microsoft.com/d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682">Creating Transform Nodes</a>



<a href="https://msdn.microsoft.com/01d7eb7c-a3d3-4924-a8ec-a67e9dc17424">IMFTopologyNode</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

