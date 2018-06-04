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

# SelectClipRgn function


## -description


The <b>SelectClipRgn</b> function selects a region as the current clipping region for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param hrgn [in]

A handle to the region to be selected.


## -returns



The return value specifies the region's complexity and can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULLREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SIMPLEREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMPLEXREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is more than one rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred. (The previous clipping region is unaffected.)

</td>
</tr>
</table>
 




## -remarks



Only a copy of the selected region is used. The region itself can be selected for any number of other device contexts or it can be deleted.

The <b>SelectClipRgn</b> function assumes that the coordinates for a region are specified in device units.

To remove a device-context's clipping region, specify a <b>NULL</b> region handle.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/5ae60181-c72e-4a28-99eb-e23d35c46685">Clipping Output</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/d222defe-2ef9-4622-b2e1-462a91cb1b0a">ExtSelectClipRgn</a>
 

 

