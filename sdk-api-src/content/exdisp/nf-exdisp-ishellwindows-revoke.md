---
UID: NF:exdisp.IShellWindows.Revoke
title: IShellWindows::Revoke (exdisp.h)
author: windows-sdk-content
description: Revokes a Shell window's registration and removes the window from the Shell windows collection.
old-location: shell\IShellWindows_Revoke.htm
tech.root: shell
ms.assetid: 66ca2569-b763-445b-b5b5-98ef32c64578
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],Revoke method, IShellWindows.Revoke, IShellWindows::Revoke, Revoke, Revoke method [Windows Shell], Revoke method [Windows Shell],IShellWindows interface, _win32_IShellWindows_Revoke, exdisp/IShellWindows::Revoke, shell.IShellWindows_Revoke
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
 - IShellWindows.Revoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
---

# IShellWindows::Revoke


## -description


Revokes a Shell window's registration and removes the window from the Shell windows collection.


## -parameters




### -param lCookie [in]

Type: <b>long*</b>

The cookie that identifies the window to un-register.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



In the context of the Shell windows collection, a <i>cookie</i> is a token that uniquely identifies a registered Shell window.

Use the <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a> method to register an open window by handle. Use the <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a> method to register a pending-open window by absolute PIDL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a>



<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>
 

 

