---
UID: NC:resapi.POPEN_V2_ROUTINE
title: POPEN_V2_ROUTINE (resapi.h)
description: Opens a resource.
helpviewer_keywords: ["CLUS_RESDLL_OPEN_RECOVER_MONITOR_STATE","OpenV2","OpenV2 callback","OpenV2 callback function [Failover Cluster]","POPEN_V2_ROUTINE","POPEN_V2_ROUTINE callback function [Failover Cluster]","mscs.openv2","resapi/OpenV2","resapi/POPEN_V2_ROUTINE"]
old-location: mscs\openv2.htm
tech.root: MsCS
ms.assetid: EA798D15-9458-4F66-8D0E-13DA383552F7
ms.date: 12/05/2018
ms.keywords: CLUS_RESDLL_OPEN_RECOVER_MONITOR_STATE, OpenV2, OpenV2 callback, OpenV2 callback function [Failover Cluster], POPEN_V2_ROUTINE, POPEN_V2_ROUTINE callback function [Failover Cluster], mscs.openv2, resapi/OpenV2, resapi/POPEN_V2_ROUTINE
f1_keywords:
- resapi/OpenV2 callback
dev_langs:
- c++
req.header: resapi.h
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
- kbSyntax
api_type:
- <TBD>
api_location:
- 
api_name:
- OpenV2 callback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# POPEN_V2_ROUTINE callback function


## -description


Opens a 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resources">resource</a>. The 
    <b>POPEN_V2_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceName [in]

The name of the resource to open.


### -param ResourceKey [in]

The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">cluster database</a> key for the 
       cluster that includes the resource represented by 
       <i>ResourceName</i>.


### -param ResourceHandle [in]

The resource handle to pass to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine_ex">SetResourceStatusEx</a> 
       callback function.


### -param OpenFlags [in] [in]

One of the following flags:



#### 0x0

TBD



#### CLUS_RESDLL_OPEN_RECOVER_MONITOR_STATE (0x00000001)

TBD


## -returns



If the operation was successful, returns a resource 
       identifier (<b>RESID</b>).

If the operation was not successful, returns 
       <b>NULL</b>. Call  <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to 
       specify that an error has occurred.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>
 

 

