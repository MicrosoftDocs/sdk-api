---
UID: NS:clusapi.RESOURCE_FAILURE_INFO
title: RESOURCE_FAILURE_INFO
author: windows-sdk-content
description: Represents information about the Failover attempts for a resource. This structure is used by the RESOURCE_FAILURE_INFO_BUFFER structure.
old-location: mscs\resource_failure_info.htm
tech.root: MsCS
ms.assetid: 3FE0CC0E-B097-48FC-882F-F6B236BB0CCB
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PRESOURCE_FAILURE_INFO, PRESOURCE_FAILURE_INFO, PRESOURCE_FAILURE_INFO structure pointer [Failover Cluster], RESOURCE_FAILURE_INFO, RESOURCE_FAILURE_INFO structure [Failover Cluster], clusapi/PRESOURCE_FAILURE_INFO, clusapi/RESOURCE_FAILURE_INFO, msclus/PRESOURCE_FAILURE_INFO, msclus/RESOURCE_FAILURE_INFO, mscs.resource_failure_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clusapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: RESOURCE_FAILURE_INFO, *PRESOURCE_FAILURE_INFO
req.redist: 
---

# RESOURCE_FAILURE_INFO structure


## -description


Represents information about the <a href="https://msdn.microsoft.com/en-us/library/Aa369573(v=VS.85).aspx">Failover</a> attempts for a resource. This structure is used by the <a href="https://msdn.microsoft.com/en-us/library/Dn622953(v=VS.85).aspx">RESOURCE_FAILURE_INFO_BUFFER</a> structure.


## -struct-fields




### -field dwRestartAttemptsRemaining

The number of remaining failover attempts that can be made on the resource during the current <a href="https://msdn.microsoft.com/en-us/library/Aa369665(v=VS.85).aspx">FailoverPeriod</a> time interval.


### -field dwRestartPeriodRemaining

The amount of time remaining for the <a href="https://msdn.microsoft.com/en-us/library/Aa369665(v=VS.85).aspx">FailoverPeriod</a>, in seconds.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn622953(v=VS.85).aspx">RESOURCE_FAILURE_INFO_BUFFER</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa373109(v=VS.85).aspx">Utility Structures</a>
 

 

