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

# LPDDENUMCALLBACKEXA callback function


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



