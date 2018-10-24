---
UID: NF:imm.ImmAssociateContext
title: ImmAssociateContext function
author: windows-sdk-content
description: Associates the specified input context with the specified window. By default, the operating system associates the default input context with each window as it is created.
old-location: intl\immassociatecontext.htm
tech.root: Intl
ms.assetid: 978ea304-c44d-4f00-b86f-932bbd5f603c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ImmAssociateContext, ImmAssociateContext function [Internationalization for Windows Applications], _win32_ImmAssociateContext, imm/ImmAssociateContext, intl.immassociatecontext
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
 - ImmAssociateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImmAssociateContext function


## -description


Associates the specified input context with the specified window. By default, the operating system associates the default input context with each window as it is created.
<div class="alert"><b>Note</b>  To specify a type of association, the application should use the <a href="https://msdn.microsoft.com/7f44d274-b5e9-4feb-acd6-5c68b3f7d868">ImmAssociateContextEx</a> function.</div><div> </div>

## -parameters




### -param HWND [in]

Handle to the window to associate with the input context.


### -param HIMC [in]

Handle to the input context. If <i>hIMC</i> is <b>NULL</b>, the function removes any association the window has with an input context. Thus IME cannot be used in the window.


## -returns



Returns the handle to the input context previously associated with the window.




## -remarks



When associating an input context with a window, an application must remove the association before destroying the input context. One way to do this is to save the handle and reassociate it to the default input context with the window.




## -see-also




<a href="https://msdn.microsoft.com/7f44d274-b5e9-4feb-acd6-5c68b3f7d868">ImmAssociateContextEx</a>



<a href="https://msdn.microsoft.com/3e23e004-514a-4021-bd20-5ac55547258f">Input Method Manager</a>



<a href="https://msdn.microsoft.com/833c07eb-0ecf-41e2-9e01-8d83e51ffcef">Input Method Manager Functions</a>
 

 

