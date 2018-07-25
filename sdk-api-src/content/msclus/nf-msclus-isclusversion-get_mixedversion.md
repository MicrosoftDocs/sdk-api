---
UID: NF:msclus.ISClusVersion.get_MixedVersion
title: ISClusVersion::get_MixedVersion
author: windows-sdk-content
description: Indicates whether more than one version of the Cluster service is present in the cluster, a state described as mixed mode.
old-location: mscs\clusversion_mixedversion.htm
old-project: mscs
ms.assetid: 20edafc7-5ff7-4a9a-b492-6e9230883643
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusVersion object [Failover Cluster],MixedVersion property, ClusVersion.MixedVersion, ISClusVersion.get_MixedVersion, ISClusVersion::get_MixedVersion, MixedVersion property [Failover Cluster], MixedVersion property [Failover Cluster],ClusVersion object, _wolf_clusversion.mixedversion, get_MixedVersion, mscs.clusversion_mixedversion
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
 - ClusVersion.MixedVersion
 - ISClusVersion.get_MixedVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion::get_MixedVersion


## -description


<p class="CCE_Message">[The <b>MixedVersion</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Indicates whether 
    more than one version of the <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> is present in 
    the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>, a state described as 
    <a href="m_gly.htm">mixed mode</a>.

This property is read-only.


## -parameters


## -remarks



For more information on mixed mode clusters and compatibility between nodes running different versions of the 
    Cluster service, see <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.

All <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> properties are static values 
    corresponding the state of the cluster when the 
    <b>ClusVersion</b> object was first created. To obtain the 
    latest version information from the cluster, create a new 
    <b>ClusVersion</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a>



<a href="https://msdn.microsoft.com/016d6c19-1f24-4c04-8665-092ebb9464b7">ClusVersion.ClusterHighestVersion</a>



<a href="https://msdn.microsoft.com/32393f01-467f-4d73-bbe7-18c428806e7c">ClusVersion.ClusterLowestVersion</a>
 

 

