---
UID: NF:shellapi.ExtractAssociatedIconExW
title: ExtractAssociatedIconExW function
author: windows-sdk-content
description: ExtractAssociatedIconEx may be altered or unavailable.
old-location: shell\ExtractAssociatedIconEx.htm
old-project: shell
ms.assetid: f32260b0-917b-4406-aeee-34f71a7c7309
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ExtractAssociatedIconEx, ExtractAssociatedIconEx function [Windows Shell], ExtractAssociatedIconExA, ExtractAssociatedIconExW, _win32_ExtractAssociatedIconEx, shell.ExtractAssociatedIconEx, shellapi/ExtractAssociatedIconEx, shellapi/ExtractAssociatedIconExA, shellapi/ExtractAssociatedIconExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ExtractAssociatedIconExW (Unicode) and ExtractAssociatedIconExA (ANSI)
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
api_name:
 - ExtractAssociatedIconEx
 - ExtractAssociatedIconExA
 - ExtractAssociatedIconExW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# ExtractAssociatedIconExW function


## -description


<p class="CCE_Message">[<b>ExtractAssociatedIconEx</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets a handle to an icon stored as a resource in a file or an icon stored in a file's associated executable file. It extends the <a href="https://msdn.microsoft.com/157ce603-9988-4cae-a2cd-51db290268c3">ExtractAssociatedIcon</a> function by retrieving the icon's ID when that icon is extracted from an executable file.


## -parameters




### -param hInst [in]

Type: <b>HINSTANCE</b>

The handle of the module from which to extract the icon.


### -param pszIconPath

TBD


### -param piIconIndex

TBD


### -param piIconId

TBD




#### - lpIconPath [in, out]

Type: <b>LPTSTR</b>

Pointer to a string that, on entry, specifies the full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. 

                    

When this function returns, if the icon handle was obtained from an executable file (either an executable file directly pointed to by this parameter or an associated executable file) the function stores the full path and file name of that executable in the buffer pointed to by this parameter.


#### - lpiIconId [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the ID of the icon whose handle is to be obtained.

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's ID within that file.


#### - lpiIconIndex [in, out]

Type: <b>LPWORD</b>

Pointer to a <b>WORD</b> value that, on entry, specifies the index of the icon whose handle is to be obtained. 

                    

When the function returns, if the icon handle was obtained from an executable file (either an executable file pointed to by <i>lpIconPath</i> or an associated executable file), this value points to the icon's index in that file.


## -returns



Type: <b>HICON</b>

Returns the icon's handle if successful, otherwise <b>NULL</b>.




## -remarks



The icon handle returned by this function must be released by calling <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> when it is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/157ce603-9988-4cae-a2cd-51db290268c3">ExtractAssociatedIcon</a>



<a href="https://msdn.microsoft.com/a0314423-79d6-416e-8be0-be946477da3e">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1c4d760a-79b5-4646-9cf2-6cd32c5d05ee">ExtractIconEx</a>
 

 

