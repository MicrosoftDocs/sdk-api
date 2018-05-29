---
UID: NF:shellapi.ExtractIconW
title: ExtractIconW function
author: windows-sdk-content
description: Retrieves a handle to an icon from the specified executable file, DLL, or icon file.
old-location: menurc\extracticon.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\extracticon.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ExtractIcon, ExtractIcon function [Menus and Other Resources], ExtractIconA, ExtractIconW, _win32_ExtractIcon, _win32_extracticon_cpp, menurc.extracticon, shellapi/ExtractIcon, shellapi/ExtractIconA, shellapi/ExtractIconW, winui._win32_extracticon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractIconW (Unicode) and ExtractIconA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SHSTOCKICONID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
-	ExtractIcon
-	ExtractIconA
-	ExtractIconW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# ExtractIconW function


## -description


Retrieves a handle to an icon from the specified executable file, DLL, or icon file.

To retrieve an array of handles to large or small icons, use the <a href="https://msdn.microsoft.com/ef7a141f-9711-4345-8035-b7ad18a37caf">ExtractIconEx</a> function.


## -parameters




### -param hInst

Type: <b>HINSTANCE</b>

A handle to the instance of the application calling the function. 


### -param pszExeFileName

TBD


### -param nIconIndex [in]

Type: <b>UINT</b>

The zero-based index of the icon to retrieve. For example, if this value is 0, the function returns a handle to the first icon in the specified file.

If this value is -1, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of <b>RT_GROUP_ICON</b> resources. If the file is an .ICO file, the return value is 1. 

 If this value is a negative number not equal to –1, the function returns a handle to the icon in the specified file whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, you should use –3 to extract the icon whose resource identifier is 3. To extract the icon whose resource identifier is 1, use the <a href="https://msdn.microsoft.com/ef7a141f-9711-4345-8035-b7ad18a37caf">ExtractIconEx</a> function. 


#### - lpszExeFileName [in]

Type: <b>LPCTSTR</b>

The name of an executable file, DLL, or icon file. 


## -returns



Type: <b>HICON</b>

The return value is a handle to an icon. If the file specified was not an executable file, DLL, or icon file, the return is 1. If no icons were found in the file, the return value is <b>NULL</b>.




## -remarks



You must destroy the icon handle returned by <b>ExtractIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

