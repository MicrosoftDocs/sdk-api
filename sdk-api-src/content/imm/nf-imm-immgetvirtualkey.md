---
UID: NF:imm.ImmGetVirtualKey
title: ImmGetVirtualKey function
author: windows-sdk-content
description: Retrieves the original virtual key value associated with a key input message that the IME has already processed.
old-location: intl\immgetvirtualkey.htm
tech.root: Intl
ms.assetid: 56c40e55-19e3-4c06-bac7-c4d0098e932a
ms.author: windowssdkdev
ms.date: 08/17/2018
ms.keywords: ImmGetVirtualKey, ImmGetVirtualKey function [Internationalization for Windows Applications], _win32_ImmGetVirtualKey, imm/ImmGetVirtualKey, intl.immgetvirtualkey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: imm.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmGetVirtualKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmGetVirtualKey function


## -description


Retrieves the original virtual key value associated with a key input message that the IME has already processed.


## -parameters




### -param HWND [in]

Handle to the window that receives the key message.


## -returns



If <a href="_win32_TranslateMessage">TranslateMessage</a> has been called by the application, <b>ImmGetVirtualKey</b> returns VK_PROCESSKEY; otherwise, it returns the virtual key.




## -remarks



Although the IME sets the virtual key value to VK_PROCESSKEY after processing a key input message, an application can recover the original virtual key value with the <b>ImmGetVirtualKey</b> function. This function is used only for key input messages containing the VK_PROCESSKEY value. Applications can only get the original virtual key by using this function after receiving 

the <a href="_win32_WM_KEYDOWN">WM_KEYDOWN</a> (VK_PROCESSKEY) message, and before <a href="_win32_TranslateMessage">TranslateMessage</a> is called in its own 

message loop.




## -see-also




<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

