---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _DRVFN structure


## -description


The DRVFN structure is used by graphics drivers to provide GDI with pointers to the graphics DDI functions defined by the driver.


## -struct-fields




### -field iFunc

Is the function index that identifies a graphics DDI function implemented by the driver. The index name reflects the name of the related graphics DDI function; for example, an index value of INDEX_DrvEnablePDEV specifies the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> function. See the header file, <i>winddi.h</i>, for a complete list of index values.


### -field pfn

Specifies the address of the driver-defined graphics DDI function associated with the index supplied for <b>iFunc</b>. This function has the following prototype:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>LONG_PTR  (APIENTRY * PFN) ();</pre>
</td>
</tr>
</table></span></div>

## -remarks



A graphics driver must allocate an array of DRVFN structures, with an array element for each graphics DDI function implemented in the driver. The driver returns the array's address to GDI in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556206">DRVENABLEDATA</a> structure whose pointer is passed to the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556210">DrvEnableDriver</a> function during driver initialization.

Graphics DDI function addresses can be placed in the DRVFN array in any order.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556210">DrvEnableDriver</a>
 

 

