---
UID: NF:shlwapi.SHCreateShellPalette
title: SHCreateShellPalette function
author: windows-driver-content
description: Creates a halftone palette for the specified device context.
old-location: shell\SHCreateShellPalette.htm
old-project: shell
ms.assetid: 49afb04a-34e3-4696-a046-bc9308ae7adf
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SHCreateShellPalette, SHCreateShellPalette function [Windows Shell], _win32_SHCreateShellPalette, shell.SHCreateShellPalette, shlwapi/SHCreateShellPalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	Ext-MS-Win-Shell-ShlwApi-l1-1-1.dll
-	Ext-MS-Win-Shell-ShlwAPI-L1-1-2.dll
api_name:
-	SHCreateShellPalette
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# SHCreateShellPalette function


## -description


Creates a halftone palette for the specified device context.


## -parameters




### -param hdc [in, optional]

Type: <b>HDC</b>

The device context.


## -returns



Type: <b>HPALETTE</b>

Returns the palette if successful; otherwise 0.




## -remarks



This function behaves the same as <a href="https://msdn.microsoft.com/ba9dfa0c-98df-4922-acba-d00e9b4b0fb0">CreateHalftonePalette</a>. The palette that is returned depends on the device context in the following way:

				

<ul>
<li>If <i>hdc</i> is set to <b>NULL</b>, a full palette is returned.</li>
<li>If the device context is indexed, a full palette is returned.</li>
<li>If the device context is not indexed, a default palette (VGA colors) is returned.</li>
</ul>


