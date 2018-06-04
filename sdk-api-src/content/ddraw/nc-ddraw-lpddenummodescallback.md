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

# LPDDENUMMODESCALLBACK callback function


## -description


Do not use. This callback function is superseded by the <a href="https://msdn.microsoft.com/53185A9A-EBA3-4443-8E76-AC85E69B39F2">EnumModesCallback2</a> function that is used with the <a href="https://msdn.microsoft.com/04ed2545-c611-435d-95ef-a0d854380a69">IDirectDraw7::EnumDisplayModes</a> method.




## -parameters




### -param Arg1


### -param Arg2








#### - lpContext [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.


#### - lpDDSurfaceDesc [in]

A pointer to a read-only <a href="https://msdn.microsoft.com/library/windows/hardware/ff550339">DDSURFACEDESC</a> structure that provides the monitor frequency and the mode that can be created.


## -returns



The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.






## -remarks



You can use the LPDDENUMMODESCALLBACK data type to declare a variable that can contain a pointer to this callback function.



