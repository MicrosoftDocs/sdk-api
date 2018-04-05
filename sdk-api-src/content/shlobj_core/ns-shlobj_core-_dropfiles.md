---
UID: NS:shlobj_core._DROPFILES
title: "_DROPFILES"
author: windows-driver-content
description: Defines the CF_HDROP clipboard format. The data that follows is a double null-terminated list of file names.
old-location: shell\DROPFILES.htm
old-project: shell
ms.assetid: e1f80529-2151-4ff6-95e0-afff67f2f117
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: "*LPDROPFILES, DROPFILES, DROPFILES structure [Windows Shell], LPDROPFILES, LPDROPFILES structure pointer [Windows Shell], _DROPFILES, _win32_DROPFILES, shell.DROPFILES, shlobj_core/DROPFILES, shlobj_core/LPDROPFILES"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: DROPFILES, *LPDROPFILES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	shlobj_core.h
api_name:
-	DROPFILES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# _DROPFILES structure


## -description


Defines the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CF_HDROP</a> clipboard format. The data that follows is a double null-terminated list of file names.


## -struct-fields




### -field pFiles

Type: <b>DWORD</b>

The offset of the file list from the beginning of this structure, in bytes.


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The drop point. The coordinates depend on <b>fNC</b>.


### -field fNC

Type: <b>BOOL</b>

A nonclient area flag. If this member is <b>TRUE</b>, <b>pt</b> specifies the screen coordinates of a point in a window's nonclient area. If it is <b>FALSE</b>, <b>pt</b> specifies the client coordinates of a point in the client area.


### -field fWide

Type: <b>BOOL</b>

A value that indicates whether the file contains ANSI or Unicode characters. If the value is zero, the file contains ANSI characters. Otherwise, it contains Unicode characters.

