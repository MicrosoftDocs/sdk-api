---
UID: NF:msclus.ISClusResource.ChangeResourceGroup
title: ISClusResource::ChangeResourceGroup
author: windows-sdk-content
description: Removes the resource from its current group and places it in a different group.
old-location: mscs\clusresource_changeresourcegroup.htm
old-project: mscs
ms.assetid: c272144f-f417-4ea5-8147-4f7bd02170b7
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ChangeResourceGroup, ChangeResourceGroup method [Failover Cluster], ChangeResourceGroup method [Failover Cluster],ClusResource class, ClusResource class [Failover Cluster],ChangeResourceGroup method, ClusResource.ChangeResourceGroup, ISClusResource.ChangeResourceGroup, ISClusResource::ChangeResourceGroup, _wolf_clusresource.changeresourcegroup, mscs.clusresource_changeresourcegroup
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
 - ClusResource.ChangeResourceGroup
 - ISClusResource.ChangeResourceGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::ChangeResourceGroup


## -description


<p class="CCE_Message">[The 
    <b>ChangeResourceGroup</b> method is available 
     for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
     subsequent versions.]

Removes the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> from its current 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> and places it in a different group.


## -parameters




### -param pResourceGroup






#### - objResGroup

The <a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a> object that should add the 
      resource as a member.


## -returns



This method does not return a value.




## -remarks



Both groups must be hosted by the same node at the time the resource is moved.

If the resource is involved in a 
     <a href="https://msdn.microsoft.com/library/ms691748(v=VS.85).aspx">dependency relationship</a> with one or more 
     resources, all the resources in the dependency tree will change to the new group as well. For example, in the 
     situation shown in the following diagram, changing resource B to group 2 will move the entire dependency tree 
     (resources A, X, and Y) to group 2.

<img alt="" border="0" src="images/resmove.png"/>

For more information, see 
     <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">Resource Dependencies</a>.




## -see-also




<a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

