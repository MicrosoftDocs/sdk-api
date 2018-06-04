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

# _PSFEATURE_CUSTPAPER structure


## -description



The <b>PSFEATURE_CUSTPAPER</b> structure contains information about a custom paper size for a PostScript driver. This structure is used with the <a href="https://msdn.microsoft.com/0824b854-a4ed-4e09-a665-b7ec3dd99671">GET_PS_FEATURESETTING</a> printer escape function.




## -struct-fields




### -field lOrientation

Indicates the custom paper orientation. This member can be 0 to 3 if custom page size is selected. Otherwise, it is 1 and all other structure members are zero


### -field lWidth

Custom page width, in points.


### -field lHeight

Custom page height, in points.


### -field lWidthOffset

Custom page width offset, in points.


### -field lHeightOffset

Custom page height offset, in points.


## -remarks



For the semantics of the <b>lOrientation</b>, <b>lWidth</b>, <b>lHeight</b>, <b>lWidthOffset</b>, and <b>lHeightOffset</b> members, please refer to "Custom Page Size Parameters" in "PostScript Printer Description File Format Specification" v.4.3.




## -see-also




<a href="https://msdn.microsoft.com/0824b854-a4ed-4e09-a665-b7ec3dd99671">GET_PS_FEATURESETTING</a>



<a href="https://msdn.microsoft.com/3cf3a16b-194a-404e-aba7-d094364c6f05">Print Spooler API Structures</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

