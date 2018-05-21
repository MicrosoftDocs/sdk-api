---
UID: NF:exdisp.IShellWindows.Revoke
title: IShellWindows::Revoke
author: windows-driver-content
description: Revokes a Shell window's registration and removes the window from the Shell windows collection.
old-location: shell\IShellWindows_Revoke.htm
old-project: shell
ms.assetid: 66ca2569-b763-445b-b5b5-98ef32c64578
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IShellWindows interface [Windows Shell],Revoke method, IShellWindows.Revoke, IShellWindows::Revoke, Revoke, Revoke method [Windows Shell], Revoke method [Windows Shell],IShellWindows interface, _win32_IShellWindows_Revoke, exdisp/IShellWindows::Revoke, shell.IShellWindows_Revoke
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdocvw.dll
api_name:
-	IShellWindows.Revoke
product: Windows
targetos: Windows
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
req.product: Internet Explorer 5
---

# IShellWindows::Revoke


## -description


Revokes a Shell window's registration and removes the window from the Shell windows collection.


## -parameters




### -param lCookie






#### - plCookie [in]

Type: <b>long*</b>

The cookie that identifies the window to un-register.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the context of the Shell windows collection, a <i>cookie</i> is a token that uniquely identifies a registered Shell window.

Use the <a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a> method to register an open window by handle. Use the <a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a> method to register a pending-open window by absolute PIDL.




## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a>



<a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a>
 

 

