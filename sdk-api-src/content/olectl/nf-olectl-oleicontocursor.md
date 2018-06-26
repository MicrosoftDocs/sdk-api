---
UID: NF:olectl.OleIconToCursor
title: OleIconToCursor function
author: windows-sdk-content
description: Converts an icon to a cursor.
old-location: com\oleicontocursor.htm
old-project: com
ms.assetid: f5de0b9e-6e3d-424c-aeeb-1c272606aea0
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: OleIconToCursor, OleIconToCursor function [COM], _com_OleIconToCursor, com.oleicontocursor, olectl/OleIconToCursor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: olectl.h
req.include-header: 
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
req.typenames: PARAMDATA, *LPPARAMDATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleaut32.dll
api_name:
 - OleIconToCursor
product: Windows
targetos: Windows
req.lib: Oleaut32.lib
req.dll: Oleaut32.dll
req.irql: 
req.product: ADAM
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



