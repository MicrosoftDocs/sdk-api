---
UID: NF:msclus.ISClusResource.Online
title: ISClusResource::Online
author: windows-sdk-content
description: Brings the resource online.
old-location: mscs\clusresource_online.htm
old-project: mscs
ms.assetid: 64f63071-b07d-4391-9631-a7a1dae35dc5
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusResource class [Failover Cluster],Online method, ClusResource.Online, ISClusResource.Online, ISClusResource::Online, Online, Online method [Failover Cluster], Online method [Failover Cluster],ClusResource class, _wolf_clusresource.online, mscs.clusresource_online
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
 - ClusResource.Online
 - ISClusResource.Online
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::Online


## -description


<p class="CCE_Message">[The <b>Online</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]


    Brings the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">online</a>.


## -parameters




### -param nTimeout




### -param pvarPending






#### - varPending

A <b>Variant</b> set to <b>TRUE</b> if the request is still 
      pending.


#### - varTimeout

A <b>Variant</b> that specifies how long (in seconds) the method should wait for the 
      resource to come online before setting <i>varPending</i> to <b>TRUE</b> 
      and returning.


## -returns



This method does not return a value.




## -remarks



Any resources that the resource <a href="https://msdn.microsoft.com/library/ms691748(v=VS.85).aspx">depends</a> 
    on are brought online first.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

