---
UID: NS:clusapi.RESOURCE_FAILURE_INFO
title: RESOURCE_FAILURE_INFO
author: windows-sdk-content
description: Represents information about the Failover attempts for a resource. This structure is used by the RESOURCE_FAILURE_INFO_BUFFER structure.
old-location: mscs\resource_failure_info.htm
old-project: mscs
ms.assetid: 3FE0CC0E-B097-48FC-882F-F6B236BB0CCB
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PRESOURCE_FAILURE_INFO, PRESOURCE_FAILURE_INFO, PRESOURCE_FAILURE_INFO structure pointer [Failover Cluster], RESOURCE_FAILURE_INFO, RESOURCE_FAILURE_INFO structure [Failover Cluster], clusapi/PRESOURCE_FAILURE_INFO, clusapi/RESOURCE_FAILURE_INFO, msclus/PRESOURCE_FAILURE_INFO, msclus/RESOURCE_FAILURE_INFO, mscs.resource_failure_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RESOURCE_FAILURE_INFO, *PRESOURCE_FAILURE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - RESOURCE_FAILURE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# RESOURCE_FAILURE_INFO structure


## -description


Represents information about the <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">Failover</a> attempts for a resource. This structure is used by the <a href="https://msdn.microsoft.com/131EEF4A-DB1E-4FF7-8329-4AA422AB83B0">RESOURCE_FAILURE_INFO_BUFFER</a> structure.


## -struct-fields




### -field dwRestartAttemptsRemaining

The number of remaining failover attempts that can be made on the resource during the current <a href="https://msdn.microsoft.com/5277a4a7-2866-4c16-8ad0-ea3a33714583">FailoverPeriod</a> time interval.


### -field dwRestartPeriodRemaining

The amount of time remaining for the <a href="https://msdn.microsoft.com/5277a4a7-2866-4c16-8ad0-ea3a33714583">FailoverPeriod</a>, in seconds.


## -see-also




<a href="https://msdn.microsoft.com/131EEF4A-DB1E-4FF7-8329-4AA422AB83B0">RESOURCE_FAILURE_INFO_BUFFER</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

