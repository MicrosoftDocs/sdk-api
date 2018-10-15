---
UID: NF:exdisp.IShellWindows.Register
title: IShellWindows::Register
author: windows-sdk-content
description: Registers an open window as a Shell window; the window is specified by handle.
old-location: shell\IShellWindows_Register.htm
tech.root: shell
ms.assetid: 4545cc34-2209-41a5-ab65-283f2985cce0
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IShellWindows interface [Windows Shell],Register method, IShellWindows.Register, IShellWindows::Register, Register, Register method [Windows Shell], Register method [Windows Shell],IShellWindows interface, _win32_IShellWindows_Register, exdisp/IShellWindows::Register, shell.IShellWindows_Register
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
 - IShellWindows.Register
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
---

# IShellWindows::Register


## -description


Registers an open window as a Shell window; the window is specified by handle.


## -parameters




### -param pid [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>*</b>

The window's <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface.


### -param hwnd [in]

Type: <b>long</b>

A handle that specifies the window to register.


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

Use this method to register an open window; if the window is pending open, use <a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a> instead.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a>



<a href="https://msdn.microsoft.com/66ca2569-b763-445b-b5b5-98ef32c64578">IShellWindows::Revoke</a>
 

 

