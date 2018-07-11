---
UID: NF:shobjidl_core.INameSpaceTreeControl.Initialize
title: INameSpaceTreeControl::Initialize
author: windows-sdk-content
description: Initializes an INameSpaceTreeControl object.
old-location: shell\INameSpaceTreeControl_Initialize.htm
old-project: shell
ms.assetid: dfc602bd-6e4e-492d-8bf4-1499319adee7
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: INameSpaceTreeControl interface [Windows Shell],Initialize method, INameSpaceTreeControl.Initialize, INameSpaceTreeControl::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],INameSpaceTreeControl interface, _shell_INameSpaceTreeControl_Initialize, shell.INameSpaceTreeControl_Initialize, shobjidl_core/INameSpaceTreeControl::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - shobjidl_core.h
api_name:
 - INameSpaceTreeControl.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# INameSpaceTreeControl::Initialize


## -description


Initializes an <a href="https://msdn.microsoft.com/2072cb3c-e540-4708-bfe8-33fff3a190bd">INameSpaceTreeControl</a> object.


## -parameters




### -param hwndParent [in]

Type: <b>HWND</b>

The handle of the parent window.


### -param prc [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that describes the size and position of the control in the client window.


### -param nsctsFlags [in]

Type: <b><a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a></b>

The characteristics of the given namespace tree control. One or more of the following values from the <a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a> enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



