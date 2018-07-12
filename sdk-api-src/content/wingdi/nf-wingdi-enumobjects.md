---
UID: NF:wingdi.EnumObjects
title: EnumObjects function
author: windows-sdk-content
description: The EnumObjects function enumerates the pens or brushes available for the specified device context (DC).
old-location: gdi\enumobjects.htm
old-project: gdi
ms.assetid: 2a7b60b2-9a68-4c56-9376-c1b780488535
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: EnumObjects, EnumObjects function [Windows GDI], _win32_EnumObjects, gdi.enumobjects, wingdi/EnumObjects
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-L1-2-1.dll
 - GDI32Full.dll
api_name:
 - EnumObjects
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# EnumObjects function


## -description


The <b>EnumObjects</b> function enumerates the pens or brushes available for the specified device context (DC). This function calls the application-defined callback function once for each available object, supplying data describing that object. <b>EnumObjects</b> continues calling the callback function until the callback function returns zero or until all of the objects have been enumerated.


## -parameters




### -param hdc [in]

A handle to the DC.


### -param nType

TBD


### -param lpFunc

TBD


### -param lParam [in]

A pointer to the application-defined data. The data is passed to the callback function along with the object information.


#### - lpObjectFunc [in]

A pointer to the application-defined callback function. For more information about the callback function, see the <a href="https://msdn.microsoft.com/05a0f329-add9-4e92-9a9a-e2cf0ba5a1c3">EnumObjectsProc</a> function.


#### - nObjectType [in]

The object type. This parameter can be OBJ_BRUSH or OBJ_PEN.


## -returns



If the function succeeds, the return value is the last value returned by the callback function. Its meaning is user-defined.

If the objects cannot be enumerated (for example, there are too many objects), the function returns zero without calling the callback function.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/05a0f329-add9-4e92-9a9a-e2cf0ba5a1c3">EnumObjectsProc</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>
 

 

