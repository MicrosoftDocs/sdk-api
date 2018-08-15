---
UID: NF:msclus.ISClusResGroup.Offline
title: ISClusResGroup::Offline
author: windows-sdk-content
description: Takes a group &#32; offline.
old-location: mscs\clusresgroup_offline.htm
old-project: mscs
ms.assetid: ca4b8bd9-26fb-40f6-86f7-bbd1514fc9ac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResGroup class [Failover Cluster],Offline method, ClusResGroup.Offline, ISClusResGroup.Offline, ISClusResGroup::Offline, Offline, Offline method [Failover Cluster], Offline method [Failover Cluster],ClusResGroup class, _wolf_clusresgroup.offline, mscs.clusresgroup_offline
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
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
 - ClusResGroup.Offline
 - ISClusResGroup.Offline
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroup::Offline


## -description


<p class="CCE_Message">[The <b>Offline</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Takes a <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">group</a>
<a href="o_gly.htm">offline</a>.


## -parameters




### -param varTimeout

A <b>Variant</b> that specifies how long (in seconds) the method should wait for the 
      group to come offline before setting <i>varPending</i> to <b>TRUE</b> and 
      returning.


### -param pvarPending






#### - varPending

A <b>Variant</b> set to <b>TRUE</b> if the request is still 
      pending.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a>



<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a>
 

 

