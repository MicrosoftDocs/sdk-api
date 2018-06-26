---
UID: NF:winuser.UnloadKeyboardLayout
title: UnloadKeyboardLayout function
author: windows-sdk-content
description: Unloads an input locale identifier (formerly called a keyboard layout).
old-location: inputdev\unloadkeyboardlayout.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\unloadkeyboardlayout.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: UnloadKeyboardLayout, UnloadKeyboardLayout function [Keyboard and Mouse Input], _win32_UnloadKeyboardLayout, _win32_unloadkeyboardlayout_cpp, inputdev.unloadkeyboardlayout, winui._win32_unloadkeyboardlayout, winuser/UnloadKeyboardLayout
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - UnloadKeyboardLayout
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UnloadKeyboardLayout function


## -description


Unloads an input locale identifier (formerly called a keyboard layout). 


## -parameters




### -param hkl [in]

Type: <b>HKL</b>

The input locale identifier to be unloaded. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The function can fail for the following reasons: 

<ul>
<li>An invalid input locale identifier was passed.</li>
<li>The input locale identifier was preloaded.</li>
<li>The input locale identifier is in use.</li>
</ul>
To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input. 

<b>UnloadKeyboardLayout</b> cannot unload the system default input locale identifier if it is the only keyboard layout loaded. You must first load another input locale identifier before unloading the default input locale identifier.




## -see-also




<a href="https://msdn.microsoft.com/bfc045fb-8696-45f5-b65f-06a08c000765">ActivateKeyboardLayout</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/505e053b-0f3d-47ad-b4ab-37bfae2512ef">GetKeyboardLayoutName</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<a href="https://msdn.microsoft.com/6e35847e-d641-4ff2-80b6-a5b5293ebbdc">LoadKeyboardLayout</a>



<b>Reference</b>
 

 

