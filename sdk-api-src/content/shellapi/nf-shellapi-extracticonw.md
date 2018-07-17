---
UID: NF:shellapi.ExtractIconW
title: ExtractIconW function
author: windows-sdk-content
description: Gets a handle to an icon from the specified executable file, DLL, or icon file. To retrieve an array of handles to large or small icons, use the ExtractIconEx function.
old-location: shell\ExtractIcon.htm
old-project: shell
ms.assetid: a0314423-79d6-416e-8be0-be946477da3e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ExtractIcon, ExtractIcon function [Windows Shell], ExtractIconA, ExtractIconW, _shell_ExtractIcon, shell.ExtractIcon, shellapi/ExtractIcon, shellapi/ExtractIconA, shellapi/ExtractIconW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: SHSTOCKICONID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - ExtractIcon
 - ExtractIconA
 - ExtractIconW
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# ExtractIconW function


## -description


Gets a handle to an icon from the specified executable file, DLL, or icon file.

            

To retrieve an array of handles to large or small icons, use the <a href="https://msdn.microsoft.com/1c4d760a-79b5-4646-9cf2-6cd32c5d05ee">ExtractIconEx</a> function.


## -parameters




### -param hInst [in]

Type: <b>HINSTANCE</b>

Handle to the instance of the application that calls the function.


### -param pszExeFileName

TBD


### -param nIconIndex

Type: <b>UINT</b>

Specifies the zero-based index of the icon to retrieve. For example, if this value is 0, the function returns a handle to the first icon in the specified file. 
                    
                    

If this value is -1, the function returns the total number of icons in the specified file. If the file is an executable file or DLL, the return value is the number of RT_GROUP_ICON resources. If the file is an .ICO file, the return value is 1.

If this value is a negative number not equal to –1, the function returns a handle to the icon in the specified file whose resource identifier is equal to the absolute value of <i>nIconIndex</i>. For example, you should use –3 to extract the icon whose resource identifier is 3. To extract the icon whose resource identifier is 1, use the <a href="https://msdn.microsoft.com/1c4d760a-79b5-4646-9cf2-6cd32c5d05ee">ExtractIconEx</a> function.


#### - lpszExeFileName [in]

Type: <b>LPCTSTR</b>

Pointer to a null-terminated string that specifies the name of an executable file, DLL, or icon file.


## -returns



Type: <b>HICON</b>

The return value is a handle to an icon. If the file specified was not an executable file, DLL, or icon file, the return is 1. If no icons were found in the file, the return value is <b>NULL</b>.




## -remarks



When it is no longer needed, you must destroy the icon handle returned by <b>ExtractIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function.




## -see-also




<a href="https://msdn.microsoft.com/157ce603-9988-4cae-a2cd-51db290268c3">ExtractAssociatedIcon</a>



<a href="https://msdn.microsoft.com/f32260b0-917b-4406-aeee-34f71a7c7309">ExtractAssociatedIconEx</a>



<a href="https://msdn.microsoft.com/1c4d760a-79b5-4646-9cf2-6cd32c5d05ee">ExtractIconEx</a>
 

 

