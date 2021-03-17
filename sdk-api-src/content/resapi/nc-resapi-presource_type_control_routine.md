---
UID: NC:resapi.PRESOURCE_TYPE_CONTROL_ROUTINE
title: PRESOURCE_TYPE_CONTROL_ROUTINE (resapi.h)
description: Performs an operation that applies to a resource type.
helpviewer_keywords: ["PRESOURCE_TYPE_CONTROL_ROUTINE","PRESOURCE_TYPE_CONTROL_ROUTINE callback function [Failover Cluster]","ResourceTypeControl","ResourceTypeControl callback","ResourceTypeControl callback function [Failover Cluster]","_wolf_resourcetypecontrol","mscs.resourcetypecontrol","resapi/PRESOURCE_TYPE_CONTROL_ROUTINE","resapi/ResourceTypeControl"]
old-location: mscs\resourcetypecontrol.htm
tech.root: MsCS
ms.assetid: dc4a6e6e-f968-4502-88d0-dc692341528d
ms.date: 12/05/2018
ms.keywords: PRESOURCE_TYPE_CONTROL_ROUTINE, PRESOURCE_TYPE_CONTROL_ROUTINE callback function [Failover Cluster], ResourceTypeControl, ResourceTypeControl callback, ResourceTypeControl callback function [Failover Cluster], _wolf_resourcetypecontrol, mscs.resourcetypecontrol, resapi/PRESOURCE_TYPE_CONTROL_ROUTINE, resapi/ResourceTypeControl
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
 - PRESOURCE_TYPE_CONTROL_ROUTINE
 - resapi/PRESOURCE_TYPE_CONTROL_ROUTINE
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
 - ResourceTypeControl
---

# PRESOURCE_TYPE_CONTROL_ROUTINE callback function


## -description

Performs an operation that applies to a 
    <a href="/previous-versions/windows/desktop/mscs/resource-types">resource type</a>. The 
    <b>PRESOURCE_TYPE_CONTROL_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param ResourceTypeName [in]

Type of resource to be affected by the operation.

### -param ControlCode [in]

<a href="/previous-versions/windows/desktop/mscs/about-control-codes">Control code</a> that represents the operation to be 
       performed. For a list of valid values for the <i>ControlCode</i> parameter, see 
       <a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">Resource Type Control Codes</a>.

### -param InBuffer [in]

Pointer to a buffer containing data to be used in the operation. <i>InBuffer</i> can be 
       <b>NULL</b> if the operation does not require data.

### -param InBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>InBuffer</i>.

### -param OutBuffer [out]

Pointer to a buffer containing data resulting from the operation. <i>OutBuffer</i> can be 
       <b>NULL</b> if the operation returns no data.

### -param OutBufferSize [in]

Size, in bytes, of the available space pointed to by <i>OutBuffer</i>.

### -param BytesReturned [out]

Number of bytes in the buffer pointed to by <i>OutBuffer</i> that actually contain 
       data.

## -returns

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following is a possible error 
       code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The resource DLL requested that the 
         <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> perform default processing (if any) 
         for <i>ControlCode</i> in addition to processing supplied by the DLL (if any).

</td>
</tr>
</table>

## -remarks

Some control codes should be handled by the <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>, 
     while others should be left to the Resource Monitor. For effective implementation strategies of the 
     <b>ResourceTypeControl</b> entry-point function, see 
     <a href="/previous-versions/windows/desktop/mscs/implementing-resourcetypecontrol">Implementing ResourceTypeControl</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>