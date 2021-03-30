---
UID: NC:resapi.PSTARTUP_EX_ROUTINE
title: PSTARTUP_EX_ROUTINE (resapi.h)
description: Loads a resource DLL, returning a structure that contains a function table and a version number.
helpviewer_keywords: ["PSTARTUP_EX_ROUTINE","PSTARTUP_EX_ROUTINE callback function [Failover Cluster]","StartupEx","StartupEx callback","StartupEx callback function [Failover Cluster]","mscs.startupex","resapi/PSTARTUP_EX_ROUTINE","resapi/StartupEx"]
old-location: mscs\startupex.htm
tech.root: MsCS
ms.assetid: 7C669EDC-B7A1-4623-91A9-5D8C5949B50A
ms.date: 12/05/2018
ms.keywords: PSTARTUP_EX_ROUTINE, PSTARTUP_EX_ROUTINE callback function [Failover Cluster], StartupEx, StartupEx callback, StartupEx callback function [Failover Cluster], mscs.startupex, resapi/PSTARTUP_EX_ROUTINE, resapi/StartupEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSTARTUP_EX_ROUTINE
 - resapi/PSTARTUP_EX_ROUTINE
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - StartupEx callback
---

# PSTARTUP_EX_ROUTINE callback function


## -description

Loads a <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>, returning a structure 
    that contains a function table and a version number. The <b>PSTARTUP_EX_ROUTINE</b> 
    type defines a pointer to this function.

## -parameters

### -param ResourceType [in]

The type of resource to start.

### -param MinVersionSupported [in]

The minimum version of the <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> supported by the 
       <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>.

### -param MaxVersionSupported [in]

The maximum version of the Resource API supported by the Cluster service.

### -param MonitorCallbackFunctions [in] [in]

TBD

### -param ResourceDllInterfaceFunctions [out] [out]

TBD

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The request was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
<dt>1306 (0x51A)</dt>
</dl>
</td>
<td width="60%">
The resource DLL does not support a version that falls in the range identified by the 
         <i>MinVersionSupported</i> and <i>MaxVersionSupported</i> 
         parameters.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>
