---
UID: NF:msclus.ISClusResource.CanResourceBeDependent
title: ISClusResource::CanResourceBeDependent
author: windows-sdk-content
description: Determines if the resource can be dependent on another resource.
old-location: mscs\clusresource_canresourcebedependent.htm
old-project: mscs
ms.assetid: d167192f-4577-49b6-aa1c-1dbd6d2aa98c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CanResourceBeDependent, CanResourceBeDependent method [Failover Cluster], CanResourceBeDependent method [Failover Cluster],ClusResource class, ClusResource class [Failover Cluster],CanResourceBeDependent method, ClusResource.CanResourceBeDependent, ISClusResource.CanResourceBeDependent, ISClusResource::CanResourceBeDependent, _wolf_clusresource.canresourcebedependent, mscs.clusresource_canresourcebedependent
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
 - ClusResource.CanResourceBeDependent
 - ISClusResource.CanResourceBeDependent
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::CanResourceBeDependent


## -description


<p class="CCE_Message">[The 
    <b>CanResourceBeDependent</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Determines if the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> can be 
    <a href="https://msdn.microsoft.com/en-us/library/Aa369367(v=VS.85).aspx">dependent</a> on another resource.


## -parameters




### -param pResource




### -param pvarDependent






#### - objResource

The <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object upon which this 
      resource may or may not depend.


## -returns



A <b>Variant</b> set to <b>TRUE</b> if this resource can depend on 
      the resource identified by <i>objResource</i>; otherwise, it is 
      <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

