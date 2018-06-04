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

# IVPBaseConfig::GetVideoFormats


## -description



The <code>GetVideoFormats</code> method retrieves the video formats the driver supports.




## -parameters




### -param pdwNumFormats [in, out]

Pointer to a variable that specifies the number of <b>DDPIXELFORMAT</b> structures in the <i>pddPixelFormats</i> array. On input, specifies the size of the array (in number of array elements). On output, contains the actual number of <b>DDPIXELFORMAT</b> structures that were copied into the array. If <i>pddPixelFormat</i> is <b>NULL</b>, the method returns the required array size.


### -param pddPixelFormats [in, out]

Pointer to an array of <b>DDPIXELFORMAT</b> structures, allocated by the caller. The device fills in the array with the format information.


## -returns



Returns S_OK if successful, or an error code otherwise.




## -remarks



The client first calls this method with the value <b>NULL</b> for the <i>pddPixelFormats</i> parameter. The device returns the number of <b>DDPIXELFORMAT</b> structures in the <i>pddPixelFormatso</i> parameter. The client allocates an array of that size, and calls the method again, passing the address of the array in the <i>pddPixelFormats</i> parameter. The device copies the format information into the buffer, and returns the actual number of copied structures in the <i>pddPixelFormats</i> parameter.

The <b>DDPIXELFORMAT</b> structure is documented in the Windows DDK.

The client sets the format by calling the <a href="https://msdn.microsoft.com/98b4182f-c286-4f4a-86b8-40d093456628">IVPBaseConfig::SetVideoFormat</a> method with an index number, which references one of the format structures returned by this method.

Include Dvp.h and Vptype.h before Vpconfig.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d9a4f395-3d2f-429a-884d-90131927a929">IVPBaseConfig Interface</a>
 

 

