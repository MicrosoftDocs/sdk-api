---
UID: NF:msclus.ISClusVersion.get_VendorId
title: ISClusVersion::get_VendorId
author: windows-sdk-content
description: Returns vendor information about the Cluster service installed on the local node.
old-location: mscs\clusversion_vendorid.htm
old-project: mscs
ms.assetid: d7d4b2cd-bb61-429a-970a-4e69113d42a8
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusVersion object [Failover Cluster],VendorId property, ClusVersion.VendorId, ISClusVersion.get_VendorId, ISClusVersion::get_VendorId, VendorId property [Failover Cluster], VendorId property [Failover Cluster],ClusVersion object, _wolf_clusversion.vendorid, get_VendorId, mscs.clusversion_vendorid
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
 - ClusVersion.VendorId
 - ISClusVersion.get_VendorId
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion::get_VendorId


## -description


<p class="CCE_Message">[The <b>VendorId</b> property 
    is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Returns vendor 
    information about the <a href="https://msdn.microsoft.com/library/ms682005(v=VS.85).aspx">Cluster service</a> installed on 
    the local <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.

This property is read-only.


## -parameters


## -remarks



All <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> properties are static values 
    corresponding the state of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> when the 
    <b>ClusVersion</b> object was first created. To obtain the 
    latest version information from the cluster, create a new 
    <b>ClusVersion</b> object.


#### Examples

See <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> for an 
     example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a>
 

 

