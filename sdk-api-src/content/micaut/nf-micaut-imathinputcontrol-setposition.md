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

# IMathInputControl::SetPosition


## -description


Modifies the location and size of the control.


## -parameters




### -param Left [in]

The leftmost position of the control.


### -param Top [in]

The highest position of the control.


### -param Right [in]

The rightmost position of the control.


### -param Bottom [in]

The lowest position of the control.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The control was resized but the resulting width, height, or both are not equal to the input parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



This method can be called regardless of the control visibility state.

This method will succeed even if parameters are not valid. If the rectangle is larger than the maximum allowed size of the control (desktop window), the maximum possible size is used instead. If the rectangle is smaller than the minimal size of the control, or too small to keep the ink and result preview intact, the minimal possible size is used instead.


If  the method returns <b>S_FALSE</b>, the  <a href="https://msdn.microsoft.com/4928f92d-7150-434c-abe4-d65a48ce1a56">GetPosition</a> method will return the actual size characteristics of the control.




## -see-also




<a href="https://msdn.microsoft.com/4928f92d-7150-434c-abe4-d65a48ce1a56">GetPosition</a>



<a href="https://msdn.microsoft.com/3d6a6289-7be5-4cf0-8cb7-9095c4ee7149">IMathInputControl</a>
 

 

