---
UID: NF:msclus.ISClusNode.get_NodeID
title: ISClusNode::get_NodeID
author: windows-sdk-content
description: Unique identifier of a cluster node.
old-location: mscs\clusnode_nodeid.htm
old-project: mscs
ms.assetid: 8ef68a5e-e7a0-4b32-8649-4fd194520ea6
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusNode object [Failover Cluster],NodeID property, ClusNode.NodeID, ISClusNode.get_NodeID, ISClusNode::get_NodeID, NodeID property [Failover Cluster], NodeID property [Failover Cluster],ClusNode object, _wolf_clusnode.nodeid, get_NodeID, mscs.clusnode_nodeid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusNode.NodeID
 - ISClusNode.get_NodeID
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNode::get_NodeID


## -description


<p class="CCE_Message">[The <b>NodeID</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns the unique 
    identifier of a cluster <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.

This property is read-only.


## -parameters


## -remarks



The <b>NodeID</b> of a node is stored under 
    <b>HKEY_LOCAL_MACHINE</b>\<b>Cluster</b>\<b>Node</b>.

<b>NodeID</b> is not accessible through 
    <a href="https://msdn.microsoft.com/5d89c4b8-0554-4672-9e06-2ce7c5d15d5f">Cluster Administrator</a>.

Changing the name of a node does not affect its 
    <b>NodeID</b>.




## -see-also




<a href="https://msdn.microsoft.com/0222665c-f029-40d9-b568-b27ad6e78dfc">CLUSCTL_NODE_GET_ID</a>



<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>
 

 

