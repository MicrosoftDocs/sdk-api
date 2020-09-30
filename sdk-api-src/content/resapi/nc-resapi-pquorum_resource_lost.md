---
UID: NC:resapi.PQUORUM_RESOURCE_LOST
title: PQUORUM_RESOURCE_LOST (resapi.h)
description: Called when control of the quorum resource has been lost.
helpviewer_keywords: ["PQUORUM_RESOURCE_LOST","PQUORUM_RESOURCE_LOST callback function [Failover Cluster]","QuorumResourceLost","QuorumResourceLost callback","QuorumResourceLost callback function [Failover Cluster]","_wolf_quorumresourcelost","mscs.quorumresourcelost","resapi/PQUORUM_RESOURCE_LOST","resapi/QuorumResourceLost"]
old-location: mscs\quorumresourcelost.htm
tech.root: MsCS
ms.assetid: 353eaf47-f93e-4243-8bed-7b6f07513a3c
ms.date: 12/05/2018
ms.keywords: PQUORUM_RESOURCE_LOST, PQUORUM_RESOURCE_LOST callback function [Failover Cluster], QuorumResourceLost, QuorumResourceLost callback, QuorumResourceLost callback function [Failover Cluster], _wolf_quorumresourcelost, mscs.quorumresourcelost, resapi/PQUORUM_RESOURCE_LOST, resapi/QuorumResourceLost
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PQUORUM_RESOURCE_LOST
 - resapi/PQUORUM_RESOURCE_LOST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - QuorumResourceLost
---

# PQUORUM_RESOURCE_LOST callback function


## -description

Called when control of the <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a> has 
    been lost. The <b>PQUORUM_RESOURCE_LOST</b> type defines a pointer to this 
    function.

## -parameters

### -param Resource

#### - ResourceHandle [in]

Handle identifying the <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> to which this callback 
       applies. The value for <i>ResourceHandle</i> should be the handle passed in during the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> call for this resource.

## -remarks

The <i>QuorumResourceLost</i> callback function is 
     called by a <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> to notify the 
     <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> that control of the quorum resource has 
     been lost after arbitration. A pointer to the Resource Monitor's 
     <i>QuorumResourceLost</i> callback function is passed to 
     a quorum resource DLL in the call to <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>