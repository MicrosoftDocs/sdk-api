---
UID: NF:msclus.ISClusResGroup.Move
title: ISClusResGroup::Move
author: windows-sdk-content
description: Moves a group and all of its resources from one node to another.
old-location: mscs\clusresgroup_move.htm
old-project: mscs
ms.assetid: 8f923a22-31b2-4a41-b88d-8eb7bac9725e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResGroup object [Failover Cluster],Move method, ClusResGroup.Move, ISClusResGroup.Move, ISClusResGroup::Move, Move, Move method [Failover Cluster], Move method [Failover Cluster],ClusResGroup object, _wolf_clusresgroup.move, mscs.clusresgroup_move
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
 - ClusResGroup.Move
 - ISClusResGroup.Move
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroup::Move


## -description


<p class="CCE_Message">[The <b>Move</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Moves a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> and all of its 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> from one 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to another.


## -parameters




### -param varTimeout

A <b>Variant</b> that specifies how long (in seconds) the method should wait for the 
      move to complete before setting <i>varPending</i> to <b>TRUE</b> and 
      returning.


### -param varNode




### -param pvarPending






#### - objNode [optional]

Optional. A <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> object that represents the 
      node to which the group should be moved. If no node is specified, the 
      <b>Move</b> method moves the group to the best available 
      node.


## -returns



A <b>Variant</b> that is set to <b>TRUE</b> if the request is 
      still pending.




## -remarks



Unless a node is specified, <b>Move</b> automatically 
    selects the destination node on the basis of the following data:

<ul>
<li>The set of currently active nodes.</li>
<li>The group's prioritized list of 
      <a href="p_gly.htm">preferred owner</a> nodes (see 
      <a href="https://msdn.microsoft.com/5e2872a4-72db-4cd8-9fce-34c1bd701706">ClusResGroup.PreferredOwnerNodes</a>).</li>
<li>The set of nodes listed as possible owners by all resources in the group. To access the possible owners 
      list for a resource, use the 
      <a href="https://msdn.microsoft.com/591b0508-f963-4c62-afb8-1c9224299cc0">ClusResource.PossibleOwnerNodes</a> 
      property.</li>
</ul>
<b>Move</b> selects the most preferred node from the set 
    of possible active nodes. If no active nodes are listed as possible owners by all resources in the group, 
    <b>Move</b> fails.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a>
 

 

