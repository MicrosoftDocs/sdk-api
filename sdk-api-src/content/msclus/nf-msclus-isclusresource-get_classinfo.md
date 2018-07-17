---
UID: NF:msclus.ISClusResource.get_ClassInfo
title: ISClusResource::get_ClassInfo
author: windows-sdk-content
description: Resource class of the resource.
old-location: mscs\clusresource_classinfo.htm
old-project: mscs
ms.assetid: 0af280ef-ea5a-4cca-8065-2ee74d2dafc1
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: CLUS_RESCLASS_NETWORK, CLUS_RESCLASS_STORAGE, CLUS_RESCLASS_UNKNOWN, CLUS_RESCLASS_USER, ClassInfo property [Failover Cluster], ClassInfo property [Failover Cluster],ClusResource class, ClusResource class [Failover Cluster],ClassInfo property, ClusResource.ClassInfo, ISClusResource.get_ClassInfo, ISClusResource::get_ClassInfo, _wolf_clusresource.classinfo, get_ClassInfo, mscs.clusresource_classinfo
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
 - ClusResource.ClassInfo
 - ISClusResource.get_ClassInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResource::get_ClassInfo


## -description


<p class="CCE_Message">[The <b>ClassInfo</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    resource class of the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.

This property is read-only.


## -parameters


## -remarks



A <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> that defines its own resource class should 
    provide a unique identifier for the class that is set to a value greater than 
    <b>CLUS_RESCLASS_USER</b> (32768). <b>CLUS_RESCLASS_USER</b> specifies 
    the beginning for user-defined resource class identifiers.

For information on making constants defined by the Cluster Automation Server type library (MsClus.tlb) 
    available to scripts, see 
    <a href="https://msdn.microsoft.com/2ca508c9-c34a-4af5-a6c0-3d710171f3df">Creating a Cluster Automation Server Script</a>.




## -see-also




<a href="https://msdn.microsoft.com/65168256-f097-48a5-9e86-ec419ccb13bd">CLUSTER_RESOURCE_CLASS</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a>
 

 

