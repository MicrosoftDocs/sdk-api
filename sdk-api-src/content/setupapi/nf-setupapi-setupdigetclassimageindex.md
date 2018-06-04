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

# SetupDiGetClassImageIndex function


## -description


The <b>SetupDiGetClassImageIndex</b> function retrieves the index within the class image list of a specified class.


## -parameters




### -param ClassImageListData [in]

A pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff552339">SP_CLASSIMAGELIST_DATA</a> structure that describes a class image list that includes the image for the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> that is specified by the <i>ClassGuid</i> parameter. 


### -param ClassGuid [in]

A pointer to the GUID of the device setup class for which to retrieve the index of the class image in the specified class image list.


### -param ImageIndex [out]

A pointer to an INT-typed variable that receives the index of the specified class image in the class image list.


## -returns



The function returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved by a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>.




## -remarks



If the specified device setup class is not included in the specified class image list, <b>SetupDiGetClassImageIndex</b> returns the image index for the Unknown device setup class in the <i>ImageIndex</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551080">SetupDiGetClassImageList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551081">SetupDiGetClassImageListEx</a>
 

 

