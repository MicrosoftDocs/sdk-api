---
UID: NC:resapi.PRESOURCE_CONTROL_ROUTINE
title: PRESOURCE_CONTROL_ROUTINE (resapi.h)
description: Performs an operation that applies to a resource.
helpviewer_keywords: ["PRESOURCE_CONTROL_ROUTINE","PRESOURCE_CONTROL_ROUTINE callback function [Failover Cluster]","ResourceControl","ResourceControl callback","ResourceControl callback function [Failover Cluster]","_wolf_resourcecontrol","mscs.resourcecontrol","resapi/PRESOURCE_CONTROL_ROUTINE","resapi/ResourceControl"]
old-location: mscs\resourcecontrol.htm
tech.root: MsCS
ms.assetid: a9c64471-41fa-4101-9a02-ad57add8124c
ms.date: 12/05/2018
ms.keywords: PRESOURCE_CONTROL_ROUTINE, PRESOURCE_CONTROL_ROUTINE callback function [Failover Cluster], ResourceControl, ResourceControl callback, ResourceControl callback function [Failover Cluster], _wolf_resourcecontrol, mscs.resourcecontrol, resapi/PRESOURCE_CONTROL_ROUTINE, resapi/ResourceControl
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
 - PRESOURCE_CONTROL_ROUTINE
 - resapi/PRESOURCE_CONTROL_ROUTINE
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
 - ResourceControl
---

# PRESOURCE_CONTROL_ROUTINE callback function


## -description

Performs an operation that applies to a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The 
    <b>PRESOURCE_CONTROL_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param Resource [in]

Resource identifier of the affected resource.

### -param ControlCode [in]

<a href="/previous-versions/windows/desktop/mscs/about-control-codes">Control code</a> that represents the operation to be 
       performed. For a list of valid values for the <i>ControlCode</i> parameter, see 
       <a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">Resource Type Control Codes</a>.

### -param InBuffer [in, optional]

Pointer to a buffer containing data to be used in the operation. <i>InBuffer</i> can be 
       <b>NULL</b> if no data is required.

### -param InBufferSize [in]

Size, in bytes, of the buffer pointed to by <i>InBuffer</i>.

### -param OutBuffer [out, optional]

Pointer to a buffer containing data resulting from the operation. <i>OutBuffer</i> can be 
       <b>NULL</b> if the operation does not need to return data.

### -param OutBufferSize [in]

Size, in bytes, of the available space pointed to by <i>OutBuffer</i>.

### -param BytesReturned [out]

Actual size, in bytes, of the data resulting from the operation.

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
The operation associated with <i>ControlCode</i> was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> requested that the 
         <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> perform default processing (if any) 
         for <i>ControlCode</i> in addition to processing supplied by the DLL (if any).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
<dt>234 (0xEA)</dt>
</dl>
</td>
<td width="60%">
The allocated size of <i>OutBuffer</i> was too small to hold the requested data. 
         <i>BytesReturned</i> indicates the required size. Always include the terminating 
         <b>NULL</b> when calculating the byte sizes of strings.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_PROPERTIES_STORED</b></dt>
<dt>5024 (0x13A0)</dt>
</dl>
</td>
<td width="60%">
Indicates that new property values for a resource have been set in the cluster database, but the properties 
         have not yet taken effect. The new property values will be applied after the resource is taken offline and 
         brought online.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Debug/system-error-codes">Error code</a></b></dt>
</dl>
</td>
<td width="60%">
The operation was unsuccessful.

</td>
</tr>
</table>

## -remarks

Some control codes should be handled by the resource DLL, while others should be left to the Resource Monitor. 
     For effective implementation strategies of the 
     <i>ResourceControl</i> entry-point function, see 
     <a href="/previous-versions/windows/desktop/mscs/implementing-resourcecontrol">Implementing ResourceControl</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>