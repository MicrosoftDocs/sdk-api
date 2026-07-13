---
UID: NN:shobjidl_core.IShellFolder2
title: IShellFolder2 (shobjidl_core.h)
description: Extends the capabilities of IShellFolder. Its methods provide a variety of information about the contents of a Shell folder.
helpviewer_keywords: ["IShellFolder2","IShellFolder2 interface [Windows Shell]","IShellFolder2 interface [Windows Shell]","described","_win32_IShellFolder2","shell.IShellFolder2","shobjidl_core/IShellFolder2"]
old-location: shell\IShellFolder2.htm
tech.root: shell
ms.assetid: 9b008034-3576-429e-b67c-e2222592ca46
ms.date: 12/05/2018
ms.keywords: IShellFolder2, IShellFolder2 interface [Windows Shell], IShellFolder2 interface [Windows Shell],described, _win32_IShellFolder2, shell.IShellFolder2, shobjidl_core/IShellFolder2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later); Netshell.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder2
 - shobjidl_core/IShellFolder2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
 - netshell.dll
api_name:
 - IShellFolder2
---

# IShellFolder2 interface


## -description

Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>. Its methods provide a variety of information about the contents of a Shell folder.

## -inheritance

The <b>IShellFolder2</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>. <b>IShellFolder2</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement <b>IShellFolder2</b> if your namespace extension provides services to clients beyond those in <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Call <b>IShellFolder2</b> when you need detailed information on items contained by a Shell folder. This interface supersedes <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails">IShellDetails</a>.
