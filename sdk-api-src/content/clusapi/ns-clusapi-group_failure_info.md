---
UID: NS:clusapi.GROUP_FAILURE_INFO
title: GROUP_FAILURE_INFO
author: windows-sdk-content
description: Represents information about the Failover attempts for a group failure.
old-location: mscs\group_failure_info.htm
old-project: MsCS
ms.assetid: C3E7585B-21F8-4E4C-A970-C07F72C80E76
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: "*PGROUP_FAILURE_INFO, GROUP_FAILURE_INFO, GROUP_FAILURE_INFO structure [Failover Cluster], PGROUP_FAILURE_INFO, PGROUP_FAILURE_INFO structure pointer [Failover Cluster], clusapi/GROUP_FAILURE_INFO, clusapi/PGROUP_FAILURE_INFO, msclus/GROUP_FAILURE_INFO, msclus/PGROUP_FAILURE_INFO, mscs.group_failure_info"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GROUP_FAILURE_INFO, *PGROUP_FAILURE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusApi.h
 - MsClus.h
api_name:
 - GROUP_FAILURE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# GROUP_FAILURE_INFO structure


## -description


Represents information about the <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">Failover</a> attempts for a group failure.


## -struct-fields




### -field dwFailoverAttemptsRemaining

The number of remaining failover attempts that can be made on the group during the current <a href="https://msdn.microsoft.com/5277a4a7-2866-4c16-8ad0-ea3a33714583">FailoverPeriod</a>  time interval.


### -field dwFailoverPeriodRemaining

The amount of time remaining for the <a href="https://msdn.microsoft.com/5277a4a7-2866-4c16-8ad0-ea3a33714583">FailoverPeriod</a>, in hours.


## -see-also




<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility structures</a>
 

 

