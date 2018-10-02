---
UID: NF:exdisp.IShellWindows.RegisterPending
title: IShellWindows::RegisterPending
author: windows-sdk-content
description: Registers a pending window as a Shell window; the window is specified by an absolute PIDL.
old-location: shell\IShellWindows_RegisterPending.htm
tech.root: Shell
ms.assetid: 75e8b82c-a94e-4aad-a224-f12b22b8a4b2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IShellWindows interface [Windows Shell],RegisterPending method, IShellWindows.RegisterPending, IShellWindows::RegisterPending, RegisterPending, RegisterPending method [Windows Shell], RegisterPending method [Windows Shell],IShellWindows interface, _win32_IShellWindows_RegisterPending, exdisp/IShellWindows::RegisterPending, shell.IShellWindows_RegisterPending
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows.RegisterPending
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
---

# IShellWindows::RegisterPending


## -description


Registers a pending window as a Shell window; the window is specified by an absolute PIDL.


## -parameters




### -param lThreadId

TBD


### -param pvarloc [in]

Type: <b>VARIANT*</b>

A <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> of type VT_VARIANT | VT_BYREF. Set the value of <i>pvarloc</i> to an absolute <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">PIDL</a> (PIDLIST_ABSOLUTE) that specifies the window to register.


### -param pvarlocRoot [in]

Type: <b>VARIANT*</b>

Must be <b>NULL</b> or of type VT_EMPTY.


### -param swClass [in]

Type: <b>int</b>

A member of <a href="https://msdn.microsoft.com/79d4fcf3-5256-4e21-ab9a-94605e1d742f">ShellWindowTypeConstants</a> that specifies the type of window.


### -param plCookie [out]

Type: <b>long*</b>

The window's cookie.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the context of the Shell windows collection, a <i>cookie</i> is a token that uniquely identifies a registered Shell window.

Use this method to register a window that is pending open; if the window is already open, use <a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a> instead. Use <a href="https://msdn.microsoft.com/66ca2569-b763-445b-b5b5-98ef32c64578">IShellWindows::Revoke</a> to un-register a window.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a>



<a href="https://msdn.microsoft.com/66ca2569-b763-445b-b5b5-98ef32c64578">IShellWindows::Revoke</a>
 

 

