---
UID: NF:msclus.ISClusResource.Offline
title: ISClusResource::Offline
author: windows-sdk-content
description: Takes the resource offline.
old-location: mscs\clusresource_offline.htm
old-project: mscs
ms.assetid: 5c3f0129-a859-4823-bd73-0c7e004507e5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResource class [Failover Cluster],Offline method, ClusResource.Offline, ISClusResource.Offline, ISClusResource::Offline, Offline, Offline method [Failover Cluster], Offline method [Failover Cluster],ClusResource class, _wolf_clusresource.offline, mscs.clusresource_offline
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
 - ClusResource.Offline
 - ISClusResource.Offline
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::Offline


## -description


<p class="CCE_Message">[The <b>Offline</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Takes the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>
<a href="o_gly.htm">offline</a>.


## -parameters




### -param nTimeout




### -param pvarPending






#### - varPending

A <b>Variant</b> set to <b>TRUE</b> if the request is still 
      pending.


#### - varTimeout

A <b>Variant</b> that specifies how long (in seconds) the method should wait for the 
      resource to come offline before setting <i>varPending</i> to <b>TRUE</b> 
      and returning.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

