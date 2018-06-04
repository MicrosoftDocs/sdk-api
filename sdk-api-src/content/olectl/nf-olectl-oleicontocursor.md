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

# OleIconToCursor function


## -description


Converts an icon to a cursor.


## -parameters




### -param hinstExe [in]

This parameter is ignored.


### -param hIcon [in]

A handle to the icon to be converted.


## -returns



The function returns a handle to the new cursor object. The caller is responsible for deleting this cursor with the <a href="_win32_DestroyCursor_cpp">DestroyCursor</a> function. If the conversion could not be completed, the return value is <b>NULL</b>.




## -remarks



This function calls the <a href="_win32_CopyCursor_cpp">CopyCursor</a> function.



