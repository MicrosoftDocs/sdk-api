---
UID: NC:resapi.PRESOURCE_CONTROL_ROUTINE
title: PRESOURCE_CONTROL_ROUTINE
author: windows-sdk-content
description: Performs an operation that applies to a resource.
old-location: mscs\resourcecontrol.htm
tech.root: MsCS
ms.assetid: a9c64471-41fa-4101-9a02-ad57add8124c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PRESOURCE_CONTROL_ROUTINE, PRESOURCE_CONTROL_ROUTINE callback function [Failover Cluster], ResourceControl, ResourceControl callback, ResourceControl callback function [Failover Cluster], _wolf_resourcecontrol, mscs.resourcecontrol, resapi/PRESOURCE_CONTROL_ROUTINE, resapi/ResourceControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - ResourceControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRESOURCE_CONTROL_ROUTINE callback function


## -description


Performs an operation that applies to a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
    <b>PRESOURCE_CONTROL_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

Resource identifier of the affected resource.


### -param ControlCode [in]


<a href="https://msdn.microsoft.com/b8ab57bd-f83e-46c2-9c9c-02107c3881bf">Control code</a> that represents the operation to be 
       performed. For a list of valid values for the <i>ControlCode</i> parameter, see 
       <a href="https://msdn.microsoft.com/a854829d-ed05-40a0-b7c8-c3e5ab888220">Resource Type Control Codes</a>.


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
The <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> requested that the 
         <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> perform default processing (if any) 
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
<dt><b><a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">Error code</a></b></dt>
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
     <a href="https://msdn.microsoft.com/3aa4a591-b0ae-4f2f-8642-f524f7207397">Implementing ResourceControl</a>.


#### Examples

See <a href="https://msdn.microsoft.com/library/Aa372246(v=VS.85).aspx">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

