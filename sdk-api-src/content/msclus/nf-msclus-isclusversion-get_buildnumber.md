---
UID: NF:msclus.ISClusVersion.get_BuildNumber
title: ISClusVersion::get_BuildNumber
author: windows-sdk-content
description: Returns the build number of the operating system installed on the local node.
old-location: mscs\clusversion_buildnumber.htm
old-project: mscs
ms.assetid: 2862d1b8-42b6-437f-8979-e3d385905801
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BuildNumber property [Failover Cluster], BuildNumber property [Failover Cluster],ClusVersion object, ClusVersion object [Failover Cluster],BuildNumber property, ClusVersion.BuildNumber, ISClusVersion.get_BuildNumber, ISClusVersion::get_BuildNumber, _wolf_clusversion.buildnumber, get_BuildNumber, mscs.clusversion_buildnumber
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
 - ClusVersion.BuildNumber
 - ISClusVersion.get_BuildNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion::get_BuildNumber


## -description


<p class="CCE_Message">[The <b>BuildNumber</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the build 
    number of the operating system installed on the local <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.

This property is read-only.


## -parameters


## -remarks



All <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> properties are static values 
    corresponding the state of the <a href="c_gly.htm">cluster</a> when the 
    <b>ClusVersion</b> object was first created. To obtain the 
    latest version information from the cluster, create a new 
    <b>ClusVersion</b> object.


#### Examples

See <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> for an 
     example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a>



<a href="https://msdn.microsoft.com/a7f32e65-98d6-4d69-a796-c0b4bcfe8316">ClusVersion.CSDVersion</a>



<a href="https://msdn.microsoft.com/f4d81e0a-4f65-470b-9215-f1b91e582646">ClusVersion.MajorVersion</a>



<a href="https://msdn.microsoft.com/c335922c-ac62-4b37-bafb-b29d58545c85">ClusVersion.MinorVersion</a>
 

 

