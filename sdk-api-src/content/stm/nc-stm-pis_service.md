---
UID: NC:stm.PIS_SERVICE
title: PIS_SERVICE (stm.h)
author: windows-sdk-content
description: The IsService function checks whether a service of specified type and name exists in the service table, and optionally returns the service's parameters.
old-location: rras\isservice.htm
tech.root: RRAS
ms.assetid: f2d8e1f4-ce6c-429c-bb14-26c6c75eab7e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsService, IsService callback function [RAS], PIS_SERVICE, PIS_SERVICE callback, _mpr_isservice, rras.isservice, stm/IsService
ms.topic: callback
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Stm.h
api_name:
 - IsService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIS_SERVICE callback function


## -description


The 
<b>IsService</b> function checks whether a service of specified type and name exists in the service table, and optionally returns the service's parameters.


## -parameters




### -param Type [in]

Specifies the type of the service being checked.


### -param Name [in]

Specifies the name of the service being checked.


### -param Service [out]

Pointer to a structure in which to receive the information about the matching service (if any).


## -returns



The 
<b>IsService</b> function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The service exists in the table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
No such service exists, or the operation failed. Call 
<a href="https://msdn.microsoft.com/en-us/library/ms629690(v=VS.85).aspx">GetLastError</a> for more information about the failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded, but no such service exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The service type or name is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms629690(v=VS.85).aspx">GetLastError</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/37da1071-b665-405c-a4ce-f1a484aeb19b">IPX_SERVICE</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

