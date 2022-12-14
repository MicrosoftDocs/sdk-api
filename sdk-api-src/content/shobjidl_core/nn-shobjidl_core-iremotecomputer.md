---
UID: NN:shobjidl_core.IRemoteComputer
title: IRemoteComputer (shobjidl_core.h)
description: Exposes a method that enumerates or initializes a namespace extension when it is invoked on a remote object. This interface is used, for example, to initialize the remote printers virtual folder.
helpviewer_keywords: ["IRemoteComputer","IRemoteComputer interface [Windows Shell]","IRemoteComputer interface [Windows Shell]","described","_win32_IRemoteComputer","shell.IRemoteComputer","shobjidl_core/IRemoteComputer"]
old-location: shell\IRemoteComputer.htm
tech.root: shell
ms.assetid: a2137043-baee-496b-b3ad-45af5a6f123e
ms.date: 12/05/2018
ms.keywords: IRemoteComputer, IRemoteComputer interface [Windows Shell], IRemoteComputer interface [Windows Shell],described, _win32_IRemoteComputer, shell.IRemoteComputer, shobjidl_core/IRemoteComputer
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRemoteComputer
 - shobjidl_core/IRemoteComputer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRemoteComputer
---

# IRemoteComputer interface


## -description

Exposes a method that enumerates or initializes a namespace extension when it is invoked on a remote object. This interface is used, for example, to initialize the remote printers virtual folder.

## -inheritance

The <b>IRemoteComputer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRemoteComputer</b> also has these types of members:

## -remarks

Implement <b>IRemoteComputer</b> when your namespace extension may be invoked on a remote computer.

You do not call this interface directly. <b>IRemoteComputer</b> is used by the operating system only when it has confirmed that your application is aware of this interface.
