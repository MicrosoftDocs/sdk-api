---
UID: NC:ddraw.LPDDENUMCALLBACKEXW
title: LPDDENUMCALLBACKEXW (ddraw.h)
author: windows-sdk-content
description: The DDEnumCallbackEx function is an application-defined callback function for the DirectDrawEnumerateEx function.
old-location: directdraw\ddenumcallbackex.htm
tech.root: directdraw
ms.assetid: D3D31978-D450-40B3-8C61-1F2662C1BA50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DDEnumCallbackEx, DDEnumCallbackEx callback function [DirectDraw], LPDDENUMCALLBACKEX, LPDDENUMCALLBACKEX callback, LPDDENUMCALLBACKEXA, LPDDENUMCALLBACKEXW, ddraw/DDEnumCallbackEx, directdraw.ddenumcallbackex
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
 - DDEnumCallbackEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPDDENUMCALLBACKEXW callback function


## -description


The <i>DDEnumCallbackEx</i> function is an application-defined callback function for the <a href="https://msdn.microsoft.com/38edfaaf-2c19-4836-b662-343312220032">DirectDrawEnumerateEx</a> function.




## -parameters




### -param *


### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - hm [in]

Handle of the monitor that is associated with the enumerated DirectDraw object. This parameter is NULL when the enumerated DirectDraw object is for the primary device, a nondisplay device (such as a 3-D accelerator with no 2-D capabilities), or devices not attached to the desktop.


#### - lpContext [in]

A pointer to an application-defined structure to be passed to the callback function each time that the function is called.


#### - lpDriverDescription [in]

Address of a string that contains the driver description.


#### - lpDriverName [in]

Address of a string that contains the driver name.


#### - lpGUID [in]

A pointer to the unique identifier of the DirectDraw object.


## -returns



The callback function returns nonzero to continue the enumeration.

It returns zero to stop the enumeration.






## -remarks



After the <a href="https://msdn.microsoft.com/38edfaaf-2c19-4836-b662-343312220032">DirectDrawEnumerateEx</a> function completes, the pointer to the GUID at <i>lpGUID</i> is no longer valid. You must save a copy of the GUID structure itself, not the pointer, or the <a href="https://msdn.microsoft.com/67fa1cd0-e47f-4dc4-b92c-b3401b4cbb57">DirectDrawCreateEx</a> function fails.

You can use the LPDDENUMCALLBACKEX data type to declare a variable that can contain a pointer to this callback function.

If UNICODE is defined, the string values are returned as type LPWSTR, rather than LPSTR.



