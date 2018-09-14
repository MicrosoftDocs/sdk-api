---
UID: NS:clusapi.CLUS_FTSET_INFO
title: CLUS_FTSET_INFO
author: windows-sdk-content
description: Contains information about an FT (fault tolerant) set. This structure is used by the CLUSPROP_FTSET_INFO structure to create an entry in a value list.
old-location: mscs\clus_ftset_info.htm
tech.root: mscs
ms.assetid: 75F2589D-8F4F-4B65-AE05-DA48A1EED03F
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PCLUS_FTSET_INFO, CLUS_FTSET_INFO, CLUS_FTSET_INFO structure [Failover Cluster], PCLUS_FTSET_INFO, PCLUS_FTSET_INFO structure pointer [Failover Cluster], clusapi/CLUS_FTSET_INFO, clusapi/PCLUS_FTSET_INFO, mscs.clus_ftset_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 Datacenter, Windows Server 2008 R2 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_FTSET_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_FTSET_INFO, *PCLUS_FTSET_INFO
req.redist: 
---

# CLUS_FTSET_INFO structure


## -description


Contains information about an FT (fault tolerant) set. This structure is used by the <a href="https://msdn.microsoft.com/0BD016A6-B635-4514-886A-8CD136D3F715">CLUSPROP_FTSET_INFO</a> structure to create an entry in a value list.


## -struct-fields




### -field dwRootSignature

The root signature of the FT set.


### -field dwFtType

The type of fault tolerance that is supported by the FT set.


## -see-also




<a href="https://msdn.microsoft.com/0BD016A6-B635-4514-886A-8CD136D3F715">CLUSPROP_FTSET_INFO</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data structures</a>
 

 

