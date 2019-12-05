---
UID: NF:olectl.OleIconToCursor
title: OleIconToCursor function (olectl.h)
description: Converts an icon to a cursor.
old-location: com\oleicontocursor.htm
tech.root: com
ms.assetid: f5de0b9e-6e3d-424c-aeeb-1c272606aea0
ms.date: 12/05/2018
ms.keywords: OleIconToCursor, OleIconToCursor function [COM], _com_OleIconToCursor, com.oleicontocursor, olectl/OleIconToCursor
ms.topic: function
f1_keywords:
- olectl/OleIconToCursor
dev_langs:
- c++
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
req.lib: Oleaut32.lib
req.dll: Oleaut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Oleaut32.dll
api_name:
- OleIconToCursor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The function returns a handle to the new cursor object. The caller is responsible for deleting this cursor with the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-destroycursor">DestroyCursor</a> function. If the conversion could not be completed, the return value is <b>NULL</b>.




## -remarks



This function calls the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-copycursor">CopyCursor</a> function.



