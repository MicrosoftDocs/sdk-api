---
UID: NC:ddraw.LPDDENUMMODESCALLBACK
title: LPDDENUMMODESCALLBACK
author: windows-driver-content
description: Do not use. This callback function is superseded by the EnumModesCallback2 function that is used with the IDirectDraw7::EnumDisplayModes method.
old-location: directdraw\enummodescallback.htm
old-project: directdraw
ms.assetid: 5959FD6F-7C48-43EA-8C7C-BCA659D06CE2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EnumModesCallback, EnumModesCallback callback function [DirectDraw], LPDDENUMMODESCALLBACK, LPDDENUMMODESCALLBACK callback, ddraw/EnumModesCallback, directdraw.enummodescallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ddraw.h
api_name:
-	EnumModesCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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



