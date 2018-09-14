---
UID: NF:tspi.TSPI_lineGetCallStatus
title: TSPI_lineGetCallStatus function
author: windows-sdk-content
description: The TSPI_lineGetCallStatus function returns the current status of the specified call.
old-location: tspi\tspi_linegetcallstatus.htm
tech.root: TAPI
ms.assetid: 7124ef73-148f-41df-afd6-ebfa29d5cf1c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: TSPI_lineGetCallStatus, TSPI_lineGetCallStatus function [TAPI 2.2], _tspi_tspi_linegetcallstatus, tspi.tspi_linegetcallstatus, tspi/TSPI_lineGetCallStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineGetCallStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TSPI_lineGetCallStatus function


## -description


The 
<b>TSPI_lineGetCallStatus</b> function returns the current status of the specified call.


## -parameters




### -param hdCall

The service provider's handle to the call to be queried for its status. The call state of <i>hdCall</i> can be any state.


### -param lpCallStatus

A pointer to a variably sized data structure of type 
<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>. This structure is filled with call status information.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_OPERATIONUNAVAIL.




## -remarks



The following table indicates which members of the 
<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a> data structure are filled in by the service provider and which members are filled in by TAPI. The service provider must preserve (it must not overwrite) the values filled in by TAPI.

<table>
<tr>
<th>Member name</th>
<th>TAPI</th>
<th>Service provider</th>
</tr>
<tr>
<td><b>dwTotalSize;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwNeededSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwUsedSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallState;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallStateMode;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwCallPrivilege;</b></td>
<td>X</td>
<td></td>
</tr>
<tr>
<td><b>dwCallFeatures;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwDevSpecificSize;</b></td>
<td></td>
<td>X</td>
</tr>
<tr>
<td><b>dwDevSpecificOffset;</b></td>
<td></td>
<td>X</td>
</tr>
</table>
 

<b>TSPI_lineGetCallStatus</b> returns the dynamic status of a call, whereas 
<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a> returns primarily static information about a call. Call status information includes the current call state, detailed mode information related to the call while in this state (if any), as well as a list of the available TSPI functions TAPI can invoke on the call while the call is in this state.




## -see-also




<a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>



<a href="https://msdn.microsoft.com/9ef43928-05aa-4ec6-bc44-f07a63d8ecdf">TSPI_lineGetCallInfo</a>
 

 

