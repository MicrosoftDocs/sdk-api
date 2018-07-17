---
UID: NF:msclus.ISClusResGroup.Online
title: ISClusResGroup::Online
author: windows-sdk-content
description: Brings a group &#32; online.
old-location: mscs\clusresgroup_online.htm
old-project: mscs
ms.assetid: f4861817-a2f6-4b1a-b50c-f3e9119234cd
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusResGroup class [Failover Cluster],Online method, ClusResGroup.Online, ISClusResGroup.Online, ISClusResGroup::Online, Online, Online method [Failover Cluster], Online method [Failover Cluster],ClusResGroup class, _wolf_clusresgroup.online, mscs.clusresgroup_online
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
 - ClusResGroup.Online
 - ISClusResGroup.Online
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroup::Online


## -description


<p class="CCE_Message">[The <b>Online</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]


    Brings a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">online</a>.


## -parameters




### -param varTimeout

A <b>Variant</b> that specifies how long (in seconds) the method should wait for the 
      group to come online before setting <i>varPending</i> to <b>TRUE</b> and 
      returning.


### -param varNode




### -param pvarPending






#### - objNode [optional]

Optional <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> object specifying the node on 
      which the group should be brought online. If no node is specified, the 
      <b>Online</b> method brings the group online on the best 
      possible node.


## -returns



A <b>Variant</b> set to <b>TRUE</b> if the request is still 
      pending.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a>
 

 

