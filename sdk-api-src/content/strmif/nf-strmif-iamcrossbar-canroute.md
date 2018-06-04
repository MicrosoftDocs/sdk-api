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

# IAMCrossbar::CanRoute


## -description



The <code>CanRoute</code> method queries whether a specified input pin can be routed to a specified output pin.




## -parameters




### -param OutputPinIndex [in]

Specifies the index of the output pin.


### -param InputPinIndex [in]

Specifies the index of input pin.


## -returns



Returns an <b>HRESULT</b> values. Possible values include the following.

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
These two pins can be routed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
These two pins cannot be routed.

</td>
</tr>
</table>
 




## -remarks



To route the pins, call the <a href="https://msdn.microsoft.com/a3f6823d-e389-478a-b882-2556a3cbd821">IAMCrossbar::Route</a> method. Output pins and input pins are both indexed from zero. To determine the number of output and input pins, call the <a href="https://msdn.microsoft.com/66ea86a6-82c3-4f91-a2d3-a08014f555be">IAMCrossbar::get_PinCounts</a> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9eef4923-62e7-475e-85e6-de8c1eefe483">IAMCrossbar Interface</a>



<a href="https://msdn.microsoft.com/6e8ee9c3-6776-498b-ad38-36f8172a27ae">Working with Crossbars</a>
 

 

