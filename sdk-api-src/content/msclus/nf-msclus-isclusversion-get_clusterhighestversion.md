---
UID: NF:msclus.ISClusVersion.get_ClusterHighestVersion
title: ISClusVersion::get_ClusterHighestVersion
author: windows-sdk-content
description: Returns a value containing the highest version of the Cluster service with which the current cluster is compatible.
old-location: mscs\clusversion_clusterhighestversion.htm
old-project: mscs
ms.assetid: 016d6c19-1f24-4c04-8665-092ebb9464b7
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusVersion object [Failover Cluster],ClusterHighestVersion property, ClusVersion.ClusterHighestVersion, ClusterHighestVersion property [Failover Cluster], ClusterHighestVersion property [Failover Cluster],ClusVersion object, ISClusVersion.get_ClusterHighestVersion, ISClusVersion::get_ClusterHighestVersion, _wolf_clusversion.clusterhighestversion, get_ClusterHighestVersion, mscs.clusversion_clusterhighestversion
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
 - ClusVersion.ClusterHighestVersion
 - ISClusVersion.get_ClusterHighestVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion::get_ClusterHighestVersion


## -description


<p class="CCE_Message">[The 
    <b>ClusterHighestVersion</b> property is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Returns a value containing the highest version of the 
    <a href="c_gly.htm">Cluster service</a> with which the current 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> is compatible.

This property is read-only.


## -parameters


## -remarks



All <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> properties are static values 
    corresponding to the state of the cluster when the 
    <b>ClusVersion</b> object was first created. To obtain the 
    latest version information from the cluster, create a new 
    <b>ClusVersion</b> object.

The cluster dynamically maintains the 
    <b>ClusterHighestVersion</b> and 
    <a href="https://msdn.microsoft.com/32393f01-467f-4d73-bbe7-18c428806e7c">ClusVersion.ClusterLowestVersion</a> 
    values based on the versions of the Cluster service running on the active 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a>. A node can join the cluster only if its version of the Cluster 
    service is compatible with 
    <b>ClusterHighestVersion</b> and 
    <b>ClusVersion.ClusterLowestVersion</b>. For 
    more information, see <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.


#### Examples

See <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> for an 
     example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a>



<a href="https://msdn.microsoft.com/32393f01-467f-4d73-bbe7-18c428806e7c">ClusVersion.ClusterLowestVersion</a>



<a href="https://msdn.microsoft.com/20edafc7-5ff7-4a9a-b492-6e9230883643">ClusVersion.MixedVersion</a>
 

 

