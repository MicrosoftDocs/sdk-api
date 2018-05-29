---
UID: NS:shlobj._TBINFO
title: "_TBINFO"
author: windows-sdk-content
description: Used with the SFVM_GETBUTTONINFO notification to specify the number of buttons to add to the toolbar, as well as how they're added.
old-location: shell\TBINFO_str.htm
old-project: shell
ms.assetid: da82e861-129b-4536-b036-2238c9e4c84c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*LPTBINFO, TBIF_APPEND, TBIF_PREPEND, TBIF_REPLACE, TBINFO, TBINFO structure [Windows Shell], _TBINFO, _win32_TBINFO_str, shell.TBINFO_str, shlobj/TBINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj.h
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
req.typenames: TBINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Shlobj.h
api_name:
-	TBINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _TBINFO structure


## -description


Used with the <a href="https://msdn.microsoft.com/983652ed-7309-46aa-a6c9-7516411ba5ac">SFVM_GETBUTTONINFO</a> notification to specify the number of buttons to add to the toolbar, as well as how they're added.


## -struct-fields




### -field cbuttons

Type: <b>UINT</b>

The number of buttons.


### -field uFlags

Type: <b>UINT</b>

One of the following flags.



#### TBIF_APPEND (0)

Add the new buttons after the existing buttons.



#### TBIF_PREPEND (1)

Add the new buttons before the existing buttons.



#### TBIF_REPLACE (2)

Replace the existing buttons with the new buttons.

