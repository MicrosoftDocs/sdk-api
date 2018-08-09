---
UID: NF:msclus.ISClusVersion.get_Flags
title: ISClusVersion::get_Flags
author: windows-sdk-content
description: Returns flags associated with the cluster version.
old-location: mscs\clusversion_flags.htm
old-project: mscs
ms.assetid: f671f494-6c46-45e6-9756-fc27dc10783a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CLUSTER_VERSION_FLAG_MIXED_MODE, ClusVersion object [Failover Cluster],Flags property, ClusVersion.Flags, Flags property [Failover Cluster], Flags property [Failover Cluster],ClusVersion object, ISClusVersion.get_Flags, ISClusVersion::get_Flags, _wolf_clusversion.flags, get_Flags, mscs.clusversion_flags
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
 - ClusVersion.Flags
 - ISClusVersion.get_Flags
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion::get_Flags


## -description


<p class="CCE_Message">[The <b>Flags</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns flags associated with 
    the <a href="c_gly.htm">cluster version</a>.

This property is read-only.


## -parameters


## -remarks



All <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> properties are static values 
    corresponding the state of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> when the 
    <b>ClusVersion</b> object was first created. To obtain the 
    latest version information from the cluster, create a new 
    <b>ClusVersion</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a>



<a href="https://msdn.microsoft.com/a7f32e65-98d6-4d69-a796-c0b4bcfe8316">ClusVersion.CSDVersion</a>



<a href="https://msdn.microsoft.com/f4d81e0a-4f65-470b-9215-f1b91e582646">ClusVersion.MajorVersion</a>



<a href="https://msdn.microsoft.com/c335922c-ac62-4b37-bafb-b29d58545c85">ClusVersion.MinorVersion</a>
 

 

