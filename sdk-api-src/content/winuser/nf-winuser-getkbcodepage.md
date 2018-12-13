---
UID: NF:winuser.GetKBCodePage
title: GetKBCodePage function
author: windows-sdk-content
description: Retrieves the current code page.
old-location: inputdev\getkbcodepage.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkbcodepage.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetKBCodePage, GetKBCodePage function [Keyboard and Mouse Input], _win32_GetKBCodePage, _win32_getkbcodepage_cpp, inputdev.getkbcodepage, winui._win32_getkbcodepage, winuser/GetKBCodePage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetKBCodePage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetKBCodePage function


## -description


Retrieves the current code page.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should use the <a href="https://msdn.microsoft.com/e6d42641-4bbe-44d8-baea-1087e48dae7d">GetOEMCP</a> function to retrieve the OEM code-page identifier for the system.</div><div> </div>

## -parameters






## -returns



Type: <b>UINT</b>

The return value is an OEM code-page identifier, or it is the default identifier if the registry value is not readable. For a list of OEM code-page identifiers, see <a href="https://msdn.microsoft.com/5d6fc86a-f205-4d14-bb7c-ecd71682e0fe">Code Page Identifiers</a>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a28c3f08-ee76-4e3f-b14d-fabc0af98fef">GetACP</a>



<a href="https://msdn.microsoft.com/e6d42641-4bbe-44d8-baea-1087e48dae7d">GetOEMCP</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Reference</b>
 

 

