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

# DrvEscape function


## -description


The <b>DrvEscape</b> function is used for retrieving information from a device that is not available in a device-independent device driver interface; the particular query depends on the value of the <i>iEsc</i> parameter.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the surface to which the call is directed.


### -param iEsc [in]

Specifies a query. The meaning of the other parameters depends on this value. QUERYESCSUPPORT is the only predefined value; it queries whether the driver supports a particular escape function. In this case, <i>pvIn</i> points to an escape function number; <i>cjOut</i> and <i>pvOut</i> are ignored. If the specified function is supported, the return value is nonzero.


### -param cjIn [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pvIn</i>.


### -param pvIn [in]

Pointer to the input data for the call. The format of the input data depends on the query specified by the <i>iEsc</i>parameter.


### -param cjOut [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pvOut</i>.


### -param pvOut [out]

Pointer to the output buffer. The format of the output data depends on the query specified by the <i>iEsc</i> parameter.


## -returns



The return value is dependent on the query specified by the <i>iEsc</i> parameter. If the function specified in the query is not supported, the return value is zero.




## -remarks



Drawing on the device is not allowed in this function. <a href="https://msdn.microsoft.com/library/windows/hardware/ff556203">DrvDrawEscape</a> is to be used for specialized drawing support.

GDI passes data directly from a (possibly malicious) client application to the driver, which means that the <b>DrvEscape</b> function must validate all input arguments. Specifically, this function must:

<ul>
<li>
Verify that the value received in the <i>iEsc</i> parameter represents a valid query.

</li>
<li>
Verify that the size of the input buffer (the value in the <i>cjIn</i> parameter) is valid for the specified query. 

</li>
<li>
Verify that the contents of the buffer pointed to by the <i>pvIn</i> parameter are valid for the specified query.

</li>
<li>
Verify that the size of the specified output buffer (the value in the <i>cjOut</i> parameter) is valid for the specified query.

</li>
</ul>
Microsoft reserves the range 0 to 0X10000 for its escape codes. Third-party vendors are free to choose escape codes for their own use above this range. Since driver-specific escape codes may conflict with those used in other display drivers, it is important for a display driver to validate escape parameters before processing the escape. One way to do this would be to validate the input and output block sizes and the input block parameters. For added security, drivers should also include a "magic" value which must be set appropriately in every input block to ensure that the input block is from a trusted source.

<b>DrvEscape</b> is optional for all drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556203">DrvDrawEscape</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a>
 

 

