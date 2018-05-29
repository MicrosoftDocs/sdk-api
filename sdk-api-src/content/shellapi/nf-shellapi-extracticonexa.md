---
UID: NF:shellapi.ExtractIconExA
title: ExtractIconExA function
author: windows-sdk-content
description: Creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file.
old-location: menurc\extracticonex.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\extracticonex.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ExtractIconEx, ExtractIconEx function [Menus and Other Resources], ExtractIconExA, ExtractIconExW, _win32_ExtractIconEx, _win32_extracticonex_cpp, menurc.extracticonex, shellapi/ExtractIconEx, shellapi/ExtractIconExA, shellapi/ExtractIconExW, winui._win32_extracticonex
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
req.unicode-ansi: ExtractIconExW (Unicode) and ExtractIconExA (ANSI)
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
-	ExtractIconEx
-	ExtractIconExA
-	ExtractIconExW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# ExtractIconExA function


## -description


Creates an array of handles to large or small icons extracted from the specified executable file, DLL, or icon file. 


## -parameters




### -param lpszFile [in]

Type: <b>LPCTSTR</b>

The name of an executable file, DLL, or icon file from which icons will be extracted. 


### -param nIconIndex [in]

Type: <b>int</b>

The zero-based index of the first icon to extract. For example, if this value is zero, the function extracts the first icon in the specified file. 

If this value is –1 and <i>phiconLarge</i> and <i>phiconSmall</i> are both <b>NULL</b>, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of <b>RT_GROUP_ICON</b> resources. If the file is an .ico file, the return value is 1. 


						 If this value is a negative number and either <i>phiconLarge</i> or <i>phiconSmall</i> is not <b>NULL</b>, the function begins by extracting the icon whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, use -3 to extract the icon whose resource identifier is 3. 


### -param phiconLarge [out, optional]

Type: <b>HICON*</b>

An array of icon handles that receives handles to the large icons extracted from the file. If this parameter is <b>NULL</b>, no large icons are extracted from the file. 


### -param phiconSmall [out, optional]

Type: <b>HICON*</b>

An array of icon handles that receives handles to the small icons extracted from the file. If this parameter is <b>NULL</b>, no small icons are extracted from the file. 


### -param nIcons [in]

Type: <b>UINT</b>

The number of icons to be extracted from the file. 


## -returns



Type: <b>UINT</b>

If the <i>nIconIndex</i> parameter is -1, the <i>phiconLarge</i> parameter is <b>NULL</b>, and the <i>phiconSmall</i> parameter is <b>NULL</b>, then the return value is the number of icons contained in the specified file. Otherwise, the return value is the number of icons successfully extracted from the file. 




## -remarks



You must destroy all icons extracted by <b>ExtractIconEx</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 

To retrieve the dimensions of the large and small icons, use the <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a> function with the <b>SM_CXICON</b>, <b>SM_CYICON</b>, <b>SM_CXSMICON</b>, and <b>SM_CYSMICON</b> flags.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/323c5e09-4e22-4a67-b8aa-5e5f369fb585">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

