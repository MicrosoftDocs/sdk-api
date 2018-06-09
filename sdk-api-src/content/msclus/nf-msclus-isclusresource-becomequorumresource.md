---
UID: NF:msclus.ISClusResource.BecomeQuorumResource
title: ISClusResource::BecomeQuorumResource
author: windows-sdk-content
description: Establishes a resource as the quorum resource for the cluster.
old-location: mscs\clusresource_becomequorumresource.htm
old-project: MsCS
ms.assetid: fd316586-8553-4c4a-824e-ee5b7bf48184
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: BecomeQuorumResource, BecomeQuorumResource method [Failover Cluster], BecomeQuorumResource method [Failover Cluster],ClusResource object, ClusResource object [Failover Cluster],BecomeQuorumResource method, ClusResource.BecomeQuorumResource, ISClusResource.BecomeQuorumResource, ISClusResource::BecomeQuorumResource, _wolf_clusresource.becomequorumresource, mscs.clusresource_becomequorumresource
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
 - ClusResource.BecomeQuorumResource
 - ISClusResource.BecomeQuorumResource
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::BecomeQuorumResource


## -description


<p class="CCE_Message">[The 
    <b>BecomeQuorumResource</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Establishes a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as the 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> for the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -parameters




### -param bstrDevicePath




### -param lMaxLogSize

<b>Long</b> specifying the maximum size that the cluster recovery log can attain, as 
      determined by the storage capacity of the resource.


#### - strDevicePath

<b>String</b> specifying the path to the quorum resource.


## -returns



This method does not return a value.




## -remarks



Failover clusters only allow <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a> resources to 
    operate as quorum resources. However, you can enable other storage devices to act as quorum resources by creating 
    a custom resource type. For more information, see 
    <a href="https://msdn.microsoft.com/de3569ef-ee74-457e-b672-00e22ee8154c">Creating a Custom Resource Type</a> and 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">Quorum Resource</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

