---
UID: NF:shellapi.ExtractAssociatedIconA
title: ExtractAssociatedIconA function
author: windows-driver-content
description: Retrieves a handle to an indexed icon found in a file or an icon found in an associated executable file.
old-location: menurc\extractassociatedicon.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\icons\iconreference\iconfunctions\extractassociatedicon.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ExtractAssociatedIcon, ExtractAssociatedIcon function [Menus and Other Resources], ExtractAssociatedIconA, ExtractAssociatedIconW, _win32_ExtractAssociatedIcon, _win32_extractassociatedicon_cpp, menurc.extractassociatedicon, shellapi/ExtractAssociatedIcon, shellapi/ExtractAssociatedIconA, shellapi/ExtractAssociatedIconW, winui._win32_extractassociatedicon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: SHSTOCKICONID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	Ext-MS-Win-Shell-Shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
-	ExtractAssociatedIcon
-	ExtractAssociatedIconA
-	ExtractAssociatedIconW
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 5.0
---

# ExtractAssociatedIconA function


## -description


Retrieves a handle to an indexed icon found in a file or an icon found in an associated executable file. 


## -parameters




### -param hInst

Type: <b>HINSTANCE</b>

A handle to the instance of the application calling the function. 


### -param pszIconPath

TBD


### -param piIcon

TBD




#### - lpIconPath [in, out]

Type: <b>LPTSTR</b>

The full path and file name of the file that contains the icon. The function extracts the icon handle from that file, or from an executable file associated with that file. If the icon handle is obtained from an executable file, the function stores the full path and file name of that executable in the string pointed to by <i>lpIconPath</i>. 


#### - lpiIcon [in, out]

Type: <b>WORD*</b>

The index of the icon whose handle is to be obtained. If the icon handle is obtained from an executable file, the function stores the icon's identifier in this parameter. 


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is an icon handle. If the icon is extracted from an associated executable file, the function stores the full path and file name of the executable file in the string pointed to by <i>lpIconPath</i>, and stores the icon's identifier in the variable pointed to by <i>lpiIcon</i>.

If the function fails, the return value is <b>NULL</b>.




## -remarks



You must destroy the icon handle returned by <b>ExtractAssociatedIcon</b> by calling the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function. 

The <b>ExtractAssociatedIcon</b> function first looks for the indexed icon in the file specified by <i>lpIconPath</i>. If the function cannot obtain the icon handle from that file, and the file has an associated executable file, it looks in that executable file for an icon. Associations with executable files are based on file name extensions, are stored in the per-user part of the registry, and can be defined using File Manager's Associate command. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/323c5e09-4e22-4a67-b8aa-5e5f369fb585">ExtractIcon</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

