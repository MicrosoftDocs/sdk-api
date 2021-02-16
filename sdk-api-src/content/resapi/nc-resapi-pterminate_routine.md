---
UID: NC:resapi.PTERMINATE_ROUTINE
title: PTERMINATE_ROUTINE (resapi.h)
description: Immediately marks a resource as unavailable for use without waiting for cleanup processing to be completed.
helpviewer_keywords: ["PTERMINATE_ROUTINE","PTERMINATE_ROUTINE callback function [Failover Cluster]","Terminate","Terminate callback","Terminate callback function [Failover Cluster]","_wolf_terminate","mscs.terminate","resapi/PTERMINATE_ROUTINE","resapi/Terminate"]
old-location: mscs\terminate.htm
tech.root: MsCS
ms.assetid: b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3
ms.date: 12/05/2018
ms.keywords: PTERMINATE_ROUTINE, PTERMINATE_ROUTINE callback function [Failover Cluster], Terminate, Terminate callback, Terminate callback function [Failover Cluster], _wolf_terminate, mscs.terminate, resapi/PTERMINATE_ROUTINE, resapi/Terminate
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
 - PTERMINATE_ROUTINE
 - resapi/PTERMINATE_ROUTINE
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
 - Terminate
---

# PTERMINATE_ROUTINE callback function


## -description

Immediately marks a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> as unavailable for use 
    without waiting for cleanup processing to be completed. The 
    <b>PTERMINATE_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param Resource [in]

Resource identifier for the resource to be made unavailable.

## -remarks

The <i>Terminate</i> entry-point function instantly marks a 
     resource as unavailable for use. If there is a thread processing an 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> or 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> request for the resource, these requests are canceled 
     and the resource is taken offline immediately.

For effective implementation strategies of the <i>Terminate</i> 
     entry-point function, see 
     <a href="/previous-versions/windows/desktop/mscs/implementing-terminate">Implementing Terminate</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>