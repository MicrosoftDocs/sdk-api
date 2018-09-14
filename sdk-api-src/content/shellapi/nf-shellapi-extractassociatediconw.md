---
UID: NF:shellapi.ExtractAssociatedIconW
title: ExtractAssociatedIconW function
author: windows-sdk-content
description: Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file.
old-location: shell\ExtractAssociatedIcon.htm
tech.root: shell
ms.assetid: 157ce603-9988-4cae-a2cd-51db290268c3
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ExtractAssociatedIcon, ExtractAssociatedIcon function [Windows Shell], ExtractAssociatedIconA, ExtractAssociatedIconW, _shell_ExtractAssociatedIcon, shell.ExtractAssociatedIcon, shellapi/ExtractAssociatedIcon, shellapi/ExtractAssociatedIconA, shellapi/ExtractAssociatedIconW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractAssociatedIconW (Unicode) and ExtractAssociatedIconA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Ext-MS-Win-Shell-Shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - ExtractAssociatedIcon
 - ExtractAssociatedIconA
 - ExtractAssociatedIconW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ExtractAssociatedIconW function


## -description


Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file.


## -parameters




### -param hInst [in]

Type: <b>HINSTANCE</b>

A handle to the instance of the calling application.


### -param pszIconPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a string that, on entry, specifies the full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. 

                    

When this function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file) the function stores the full path and file name of that executable in the buffer pointed to by this parameter.


### -param piIcon [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the index of the icon whose handle is to be obtained. 

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's index in that file.


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is an icon handle. If the icon is extracted from an associated executable file, the function stores the full path and file name of the executable file in the string pointed to by <i>lpIconPath</i>, and stores the icon's identifier in the <b>WORD</b> pointed to by <i>lpiIcon</i>.

					

If the function fails, the return value is <b>NULL</b>.




## -remarks



When it is no longer needed, the caller is responsible for freeing the icon handle returned by <b>ExtractAssociatedIcon</b> by calling the <a href="https://msdn.microsoft.com/en-us/library/ms648063(v=VS.85).aspx">DestroyIcon</a> function.

The <b>ExtractAssociatedIcon</b> function first looks for the indexed icon in the file specified by <i>lpIconPath</i>. If the function cannot obtain the icon handle from that file, and the file has an associated executable file, it looks in that executable file for an icon. Associations with executable files are based on file name extensions and are stored in the per-user part of the registry.




## -see-also




<a href="https://msdn.microsoft.com/f32260b0-917b-4406-aeee-34f71a7c7309">ExtractAssociatedIconEx</a>



<a href="https://msdn.microsoft.com/a0314423-79d6-416e-8be0-be946477da3e">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1c4d760a-79b5-4646-9cf2-6cd32c5d05ee">ExtractIconEx</a>
 

 

