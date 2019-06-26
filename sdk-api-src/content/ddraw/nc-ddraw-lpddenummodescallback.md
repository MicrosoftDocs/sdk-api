---
UID: NC:ddraw.LPDDENUMMODESCALLBACK
title: LPDDENUMMODESCALLBACK (ddraw.h)
author: windows-sdk-content
description: Do not use. This callback function is superseded by the EnumModesCallback2 function that is used with the IDirectDraw7::EnumDisplayModes method.
old-location: directdraw\enummodescallback.htm
tech.root: directdraw
ms.assetid: 5959FD6F-7C48-43EA-8C7C-BCA659D06CE2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnumModesCallback, EnumModesCallback callback function [DirectDraw], LPDDENUMMODESCALLBACK, LPDDENUMMODESCALLBACK callback, ddraw/EnumModesCallback, directdraw.enummodescallback
ms.topic: callback
f1_keywords: 
 - "ddraw/EnumModesCallback"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ddraw.h
api_name:
 - EnumModesCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LPDDENUMMODESCALLBACK callback function


## -description


Do not use. This callback function is superseded by the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nc-ddraw-lpddenummodescallback2">EnumModesCallback2</a> function that is used with the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdraw7-enumdisplaymodes">IDirectDraw7::EnumDisplayModes</a> method.




## -parameters




### -param Arg1


### -param Arg2








#### - lpContext [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.


#### - lpDDSurfaceDesc [in]

A pointer to a read-only <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)">DDSURFACEDESC</a> structure that provides the monitor frequency and the mode that can be created.


## -returns



The callback function returns DDENUMRET_OK to continue the enumeration.

It returns DDENUMRET_CANCEL to stop the enumeration.






## -remarks



You can use the LPDDENUMMODESCALLBACK data type to declare a variable that can contain a pointer to this callback function.



