---
UID: NC:resapi.PCLOSE_ROUTINE
title: PCLOSE_ROUTINE (resapi.h)
description: Closes a resource.
helpviewer_keywords: ["Close","PCLOSE_ROUTINE","PCLOSE_ROUTINE callback","PCLOSE_ROUTINE callback function [Failover Cluster]","_wolf_close","mscs.close","resapi/PCLOSE_ROUTINE"]
old-location: mscs\close.htm
tech.root: MsCS
ms.assetid: c7c74440-c98a-4440-8bf4-10ebd1a68608
ms.date: 12/05/2018
ms.keywords: Close, PCLOSE_ROUTINE, PCLOSE_ROUTINE callback, PCLOSE_ROUTINE callback function [Failover Cluster], _wolf_close, mscs.close, resapi/PCLOSE_ROUTINE
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
 - PCLOSE_ROUTINE
 - resapi/PCLOSE_ROUTINE
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
 - PCLOSE_ROUTINE
---

# PCLOSE_ROUTINE callback function


## -description

Closes a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The 
    <b>PCLOSE_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param Resource

#### - ResourceId [in]

Resource identifier of the resource to close.

## -returns

None. Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> to specify that an error has 
       occurred.

## -remarks

For effective implementation strategies of the <b>Close</b> 
     entry-point function, see 
     <a href="/previous-versions/windows/desktop/mscs/implementing-close">Implementing Close</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>