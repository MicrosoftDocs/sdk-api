---
UID: NS:clusapi.CLUSPROP_FTSET_INFO
title: CLUSPROP_FTSET_INFO (clusapi.h)
author: windows-sdk-content
description: Contains information about an FT (fault tolerant) set. It is used as an entry in a value list and consists of a CLUSPROP_VALUE and a CLUS_FTSET_INFO structure.
old-location: mscs\clusprop_ftset_info.htm
tech.root: MsCS
ms.assetid: 0BD016A6-B635-4514-886A-8CD136D3F715
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCLUSPROP_FTSET_INFO, CLUSPROP_FTSET_INFO, CLUSPROP_FTSET_INFO structure [Failover Cluster], PCLUSPROP_FTSET_INFO, PCLUSPROP_FTSET_INFO structure pointer [Failover Cluster], clusapi/CLUSPROP_FTSET_INFO, clusapi/PCLUSPROP_FTSET_INFO, mscs.clusprop_ftset_info"
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
 - CLUSPROP_FTSET_INFO
product: Windows
targetos: Windows
req.typenames: CLUSPROP_FTSET_INFO, *PCLUSPROP_FTSET_INFO
req.redist: 
ms.custom: 19H1
---

# CLUSPROP_FTSET_INFO structure


## -description


Contains information about an FT (fault tolerant) set. It is used as an entry in a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/value-lists">value list</a> and consists of a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> and a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_ftset_info">CLUS_FTSET_INFO</a> structure.


## -struct-fields




### -field CLUSPROP_VALUE

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clusprop_value">CLUSPROP_VALUE</a> structure that describes the format, 
     type, and length of the resource class value.


### -field CLUS_FTSET_INFO

A <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/clusapi/ns-clusapi-clus_ftset_info">CLUS_FTSET_INFO</a> value that describes the 
     FT set.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/data-structures">Data structures</a>
 

 

