---
UID: NF:msclus.ISClusResGroups.CreateItem
title: ISClusResGroups::CreateItem
author: windows-sdk-content
description: Creates a group in the cluster and adds it to the ClusResGroups collection.
old-location: mscs\clusresgroups_createitem.htm
old-project: mscs
ms.assetid: 1b43a7d4-db08-402d-9910-464ba3ea8d18
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusResGroups collection [Failover Cluster],CreateItem method, ClusResGroups.CreateItem, CreateItem, CreateItem method [Failover Cluster], CreateItem method [Failover Cluster],ClusResGroups collection, ISClusResGroups.CreateItem, ISClusResGroups::CreateItem, _wolf_clusresgroups.createitem, mscs.clusresgroups_createitem
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
 - ClusResGroups.CreateItem
 - ISClusResGroups.CreateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroups::CreateItem


## -description


<p class="CCE_Message">[The <b>CreateItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Creates a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> in the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and adds it to the 
    <a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a> collection.


## -parameters




### -param bstrResourceGroupName




### -param ppResourceGroup






#### - GroupName

<b>String</b> containing the name of the group to create.


## -returns



A <a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a> object that receives the new 
      group.




## -see-also




<a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a>



<a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a>
 

 

