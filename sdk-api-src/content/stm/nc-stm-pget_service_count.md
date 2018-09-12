---
UID: NC:stm.PGET_SERVICE_COUNT
title: PGET_SERVICE_COUNT
author: windows-sdk-content
description: The GetServiceCount function returns the number of services in the table.
old-location: rras\getservicecount.htm
tech.root: RRAS
ms.assetid: 44ba90c0-a019-4aca-92e2-1e795cbd335d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetServiceCount, GetServiceCount callback function [RAS], PGET_SERVICE_COUNT, PGET_SERVICE_COUNT callback, _mpr_getservicecount, rras.getservicecount, stm/GetServiceCount
ms.prod: windows
ms.technology: windows-sdk
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
 - GetServiceCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PGET_SERVICE_COUNT callback function


## -description


The 
<b>GetServiceCount</b> function returns the number of services in the table.


## -parameters




### -param Arg1








## -returns



If the function succeeds, the return value is the number of services in the table.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Operation succeeded but no services are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0 (Zero)</b></dt>
</dl>
</td>
<td width="60%">
No services are available in the table or the operation failed. Call 
<a href="_win32_getlasterror">GetLastError</a> to obtain more information.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="_win32_getlasterror">GetLastError</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

