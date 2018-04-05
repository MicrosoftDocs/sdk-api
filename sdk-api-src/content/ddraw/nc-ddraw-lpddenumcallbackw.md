---
UID: NC:ddraw.LPDDENUMCALLBACKW
title: LPDDENUMCALLBACKW
author: windows-driver-content
description: The DDEnumCallback function is an application-defined callback function for the DirectDrawEnumerate function.
old-location: directdraw\ddenumcallback.htm
old-project: directdraw
ms.assetid: 7F86FA67-C13B-49EE-8D17-9F54E5060A85
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: DDEnumCallback, DDEnumCallback callback function [DirectDraw], LPDDENUMCALLBACK, LPDDENUMCALLBACKA, LPDDENUMCALLBACKW, ddraw/DDEnumCallback, directdraw.ddenumcallback
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
-	DDEnumCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# LPDDENUMCALLBACKW callback


## -description


The <i>DDEnumCallback</i> function is an application-defined callback function for the <a href="https://msdn.microsoft.com/1f994adb-79ff-4cc1-8769-0faeed893503">DirectDrawEnumerate</a> function.




## -parameters




### -param *


### -param Arg1


### -param Arg2


### -param Arg3








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



You can use the LPDDENUMCALLBACK data type to declare a variable that can contain a pointer to this callback function.

If UNICODE is defined, the string values are returned as type LPWSTR, rather than LPSTR.



