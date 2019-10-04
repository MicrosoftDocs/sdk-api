---
UID: NS:msclus.GROUP_FAILURE_INFO
title: GROUP_FAILURE_INFO (msclus.h)
author: windows-sdk-content
description: Represents information about the Failover attempts for a group failure.
old-location: mscs\group_failure_info.htm
tech.root: MsCS
ms.assetid: C3E7585B-21F8-4E4C-A970-C07F72C80E76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PGROUP_FAILURE_INFO, GROUP_FAILURE_INFO, GROUP_FAILURE_INFO structure [Failover Cluster], PGROUP_FAILURE_INFO, PGROUP_FAILURE_INFO structure pointer [Failover Cluster], clusapi/GROUP_FAILURE_INFO, clusapi/PGROUP_FAILURE_INFO, msclus/GROUP_FAILURE_INFO, msclus/PGROUP_FAILURE_INFO, mscs.group_failure_info"
ms.topic: struct
f1_keywords: 
 - "msclus/GROUP_FAILURE_INFO"
dev_langs:
 - c++
req.header: msclus.h
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
 - GROUP_FAILURE_INFO
targetos: Windows
req.typenames: GROUP_FAILURE_INFO, *PGROUP_FAILURE_INFO
req.redist: 
ms.custom: 19H1
---

# GROUP_FAILURE_INFO structure


## -description


Represents information about the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/failover">Failover</a> attempts for a group failure.


## -struct-fields




### -field dwFailoverAttemptsRemaining

The number of remaining failover attempts that can be made on the group during the current <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups-failoverperiod">FailoverPeriod</a>  time interval.


### -field dwFailoverPeriodRemaining

The amount of time remaining for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/groups-failoverperiod">FailoverPeriod</a>, in hours.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/utility-structures">Utility structures</a>
 

 

