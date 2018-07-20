---
UID: NS:shlobj_core.NT_FE_CONSOLE_PROPS
title: NT_FE_CONSOLE_PROPS
author: windows-sdk-content
description: Holds an extra data block used by IShellLinkDataList. It holds the console's code page.
old-location: shell\NT_FE_CONSOLE_PROPS_str.htm
old-project: shell
ms.assetid: 2f22676d-2b46-4a94-9517-64d1caeead43
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPNT_FE_CONSOLE_PROPS, LPNT_FE_CONSOLE_PROPS, LPNT_FE_CONSOLE_PROPS structure pointer [Windows Shell], NT_FE_CONSOLE_PROPS, NT_FE_CONSOLE_PROPS structure [Windows Shell], _win32_NT_FE_CONSOLE_PROPS_str, shell.NT_FE_CONSOLE_PROPS_str, shlobj_core/LPNT_FE_CONSOLE_PROPS, shlobj_core/NT_FE_CONSOLE_PROPS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
tech.root: 
req.typenames: NT_FE_CONSOLE_PROPS, *LPNT_FE_CONSOLE_PROPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - NT_FE_CONSOLE_PROPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# NT_FE_CONSOLE_PROPS structure


## -description


Holds an extra data block used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>. It holds the console's code page.


## -struct-fields




### -field dbh

Type: <b><a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a></b>

The <a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a> structure with the <b>NT_FE_CONSOLE_PROPS</b> structure's size and signature. The signature for an <b>NT_FE_CONSOLE_PROPS</b> structure is NT_FE_CONSOLE_PROPS_SIG.


### -field DUMMYSTRUCTNAME

 


### -field uCodePage

Type: <b>UINT</b>

The console's code page.

