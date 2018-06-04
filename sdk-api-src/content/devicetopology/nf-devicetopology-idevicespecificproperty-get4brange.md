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

# IDeviceSpecificProperty::Get4BRange


## -description



The <b>Get4BRange</b> method gets the 4-byte range of the device-specific property value.




## -parameters




### -param plMin [out]

Pointer to a <b>LONG</b> variable into which the method writes the minimum property value.


### -param plMax [out]

Pointer to a <b>LONG</b> variable into which the method writes the maximum property value.


### -param plStepping [out]

Pointer to a <b>LONG</b> variable into which the method writes the stepping value between consecutive property values in the range  <i>*plMin</i> to  <i>*plMax</i>. If the difference between the maximum and minimum property values is <i>d</i>, and the range is divided into <i>n</i> steps (uniformly sized intervals), then the property can take <i>n</i> + 1 discrete values and the size of the step between consecutive values is d / n.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>plMin</i>, <i>plMax</i>, or <i>plStepping</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The property value is not a 32-bit signed or unsigned integer. For information about this macro, see the Windows SDK documentation.

</td>
</tr>
</table>
 




## -remarks



This method reports the range and step size for a property value that is a 32-bit signed or unsigned integer. These two data types are represented by <b>VARENUM</b> enumeration constants VT_I4 and VT_UI4, respectively. If the property value is not a 32-bit integer, then the method returns an error status code. For more information about <b>VARENUM</b>, see the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/52873fe2-7f59-4a30-b526-cbefa27a81bb">IDeviceSpecificProperty Interface</a>
 

 

