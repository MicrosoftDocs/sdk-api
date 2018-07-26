---
UID: NF:shobjidl_core.IRemoteComputer.Initialize
title: IRemoteComputer::Initialize
author: windows-sdk-content
description: Used by Windows Explorer or Windows Internet Explorer when it is initializing or enumerating a namespace extension invoked on a remote computer.
old-location: shell\IRemoteComputer_Initialize.htm
old-project: shell
ms.assetid: 69bd0b90-dcb0-45a6-9144-294fcd2d29eb
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IRemoteComputer interface [Windows Shell],Initialize method, IRemoteComputer.Initialize, IRemoteComputer::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IRemoteComputer interface, _win32_IRemoteComputer_Initialize, shell.IRemoteComputer_Initialize, shobjidl_core/IRemoteComputer::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRemoteComputer.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IRemoteComputer::Initialize


## -description


Used by Windows Explorer or Windows Internet Explorer when it is initializing or enumerating a namespace extension invoked on a remote computer.


## -parameters




### -param pszMachine

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the machine name of the remote computer.


### -param bEnumerating

Type: <b>BOOL</b>

A value that is set to <b>TRUE</b> if Windows Explorer is enumerating the namespace extension, or <b>FALSE</b> if it is initializing it.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or standard OLE error values otherwise.




## -remarks



If failure is returned, the extension won't appear for the specified computer. Otherwise, the extension will appear and target the remote computer.



