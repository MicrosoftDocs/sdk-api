---
UID: NC:wingdi.GOBJENUMPROC
title: GOBJENUMPROC
author: windows-sdk-content
description: The EnumObjectsProc function is an application-defined callback function used with the EnumObjects function.
old-location: gdi\enumobjectsproc.htm
tech.root: gdi
ms.assetid: 05a0f329-add9-4e92-9a9a-e2cf0ba5a1c3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GOBJENUMPROC, GOBJENUMPROC callback, GOBJENUMPROC callback function [Windows GDI], _win32_EnumObjectsProc, gdi.enumobjectsproc, wingdi/GOBJENUMPROC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wingdi.h
api_name:
 - GOBJENUMPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GOBJENUMPROC callback function


## -description


The <b>EnumObjectsProc</b> function is an application-defined callback function used with the <a href="https://msdn.microsoft.com/2a7b60b2-9a68-4c56-9376-c1b780488535">EnumObjects</a> function. It is used to process the object data. The <b>GOBJENUMPROC</b> type defines a pointer to this callback function. <b>EnumObjectsProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param Arg1


### -param Arg2








#### - lpData [in]

A pointer to the application-defined data passed by the <a href="https://msdn.microsoft.com/2a7b60b2-9a68-4c56-9376-c1b780488535">EnumObjects</a> function.


#### - lpLogObject [in]

A pointer to a <a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a> or <a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a> structure describing the attributes of the object.


## -returns



To continue enumeration, the callback function must return a nonzero value. This value is user-defined.

To stop enumeration, the callback function must return zero.




## -remarks



An application must register this function by passing its address to the <a href="https://msdn.microsoft.com/2a7b60b2-9a68-4c56-9376-c1b780488535">EnumObjects</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/2a7b60b2-9a68-4c56-9376-c1b780488535">EnumObjects</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a>



<a href="https://msdn.microsoft.com/ded2c7a4-2248-4d01-95c6-ab4050719094">LOGBRUSH</a>



<a href="https://msdn.microsoft.com/0e098b5a-e249-43ad-a6d8-2509b6562453">LOGPEN</a>
 

 

