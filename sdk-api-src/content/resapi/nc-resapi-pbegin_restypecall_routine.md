---
UID: NC:resapi.PBEGIN_RESTYPECALL_ROUTINE
title: PBEGIN_RESTYPECALL_ROUTINE (resapi.h)
description: Starts a call to a resource control code. The PBEGIN_RESTYPECALL_ROUTINE type defines a pointer to this callback function.
helpviewer_keywords: ["BeginResourceTypeControl","BeginResourceTypeControl callback","BeginResourceTypeControl callback function [Failover Cluster]","PBEGIN_RESTYPECALL_ROUTINE","PBEGIN_RESTYPECALL_ROUTINE callback function [Failover Cluster]","mscs.beginresourcetypecontrol","resapi/BeginResourceTypeControl","resapi/PBEGIN_RESTYPECALL_ROUTINE"]
old-location: mscs\beginresourcetypecontrol.htm
tech.root: MsCS
ms.assetid: 9D5D5ADB-9707-4690-9B91-CC99F68DE2A8
ms.date: 12/05/2018
ms.keywords: BeginResourceTypeControl, BeginResourceTypeControl callback, BeginResourceTypeControl callback function [Failover Cluster], PBEGIN_RESTYPECALL_ROUTINE, PBEGIN_RESTYPECALL_ROUTINE callback function [Failover Cluster], mscs.beginresourcetypecontrol, resapi/BeginResourceTypeControl, resapi/PBEGIN_RESTYPECALL_ROUTINE
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
 - PBEGIN_RESTYPECALL_ROUTINE
 - resapi/PBEGIN_RESTYPECALL_ROUTINE
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
 - BeginResourceTypeControl
---

# PBEGIN_RESTYPECALL_ROUTINE callback function


## -description

Starts a call to a resource control code. The <b>PBEGIN_RESTYPECALL_ROUTINE</b> type defines a pointer to this callback function.

## -parameters

### -param ResourceTypeName [in]

The name of the resource type.

### -param ControlCode [in]

The control code to call.

### -param InBuffer [in]

A pointer to the buffer that contains the input data for the call to the control code.

### -param InBufferSize [in]

The size of the buffer specified by <i>InBuffer</i>, in bytes.

### -param OutBuffer [out]

A pointer to the buffer that contains the output data for the call to the control code.

### -param OutBufferSize [in]

The size of the buffer specified by <i>OutBuffer</i>, in bytes.

### -param BytesReturned [out]

The size of the data returned by <i>OutBuffer</i>, in bytes.

### -param context [in]

The context to the resource type control code that was called.

<b>Windows Server 2012 R2:  </b>This parameter was added in Windows Server 2016.

### -param ReturnedAsynchronously [out]

<b>TRUE</b> if the operation returns asynchronously; otherwise, <b>FALSE</b>.

<b>Windows Server 2012 R2:  </b>This parameter was added in Windows Server 2016.


#### - resCallId [in]

This parameter was removed in Windows Server 2016.

<b>Windows Server 2012 R2:  </b>This parameter is only supported in Windows Server 2012 R2.

## -returns

The function returns one of the following values, or a system error code:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The resource ID was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The requested control code is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>



<a href="/previous-versions/windows/desktop/mscs/resource-type-control-codes">Resource Type Control Codes</a>