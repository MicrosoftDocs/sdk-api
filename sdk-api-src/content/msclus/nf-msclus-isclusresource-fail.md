---
UID: NF:msclus.ISClusResource.Fail
title: ISClusResource::Fail
author: windows-sdk-content
description: Initiates failure of the resource.
old-location: mscs\clusresource_fail.htm
old-project: mscs
ms.assetid: c184a7f3-b09a-4349-a940-20d622f729a6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusResource class [Failover Cluster],Fail method, ClusResource.Fail, Fail, Fail method [Failover Cluster], Fail method [Failover Cluster],ClusResource class, ISClusResource.Fail, ISClusResource::Fail, _wolf_clusresource.fail, mscs.clusresource_fail
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
 - ClusResource.Fail
 - ISClusResource.Fail
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::Fail


## -description


<p class="CCE_Message">[The <b>Fail</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Initiates 
    <a href="https://msdn.microsoft.com/f18644d1-63ec-4920-b703-a3f149684508">failure</a> of the 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -parameters






## -returns



This method does not return a value.




## -remarks



The <b>Fail</b> method causes the 
    <a href="c_gly.htm">cluster</a> to initiate the same procedures that would result 
    if the resource had actually failed. Use the <b>Fail</b> 
    method to test <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a> policies for resources and 
    <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a>. For more information about resource failure policies, see 
    <a href="https://msdn.microsoft.com/f18644d1-63ec-4920-b703-a3f149684508">Resource Failure</a>.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

