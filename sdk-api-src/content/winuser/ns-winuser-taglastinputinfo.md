---
UID: NS:winuser.tagLASTINPUTINFO
title: tagLASTINPUTINFO
author: windows-sdk-content
description: Contains the time of the last input.
old-location: inputdev\lastinputinfo.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\lastinputinfo.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*PLASTINPUTINFO, LASTINPUTINFO, LASTINPUTINFO structure [Keyboard and Mouse Input], PLASTINPUTINFO, PLASTINPUTINFO structure pointer [Keyboard and Mouse Input], _win32_LASTINPUTINFO_str, _win32_lastinputinfo_str_cpp, inputdev.lastinputinfo, tagLASTINPUTINFO, winui._win32_lastinputinfo_str, winuser/LASTINPUTINFO, winuser/PLASTINPUTINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: LASTINPUTINFO, *PLASTINPUTINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - LASTINPUTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagLASTINPUTINFO structure


## -description


Contains the time of the last input.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the structure, in bytes. This member must be set to <code>sizeof(LASTINPUTINFO)</code>. 


### -field dwTime

Type: <b>DWORD</b>

The tick count when the last input event was received. 


## -remarks



This function is useful for input idle detection. For more information on tick counts, see <a href="https://msdn.microsoft.com/22201c82-a49a-4972-9f49-6baf6d23a1ea">GetTickCount</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b314ab8d-243f-4cd7-bb69-143076103a14">GetLastInputInfo</a>



<a href="https://msdn.microsoft.com/22201c82-a49a-4972-9f49-6baf6d23a1ea">GetTickCount</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Reference</b>
 

 

