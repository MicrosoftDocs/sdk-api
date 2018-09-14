---
UID: NF:shobjidl_core.INamespaceWalkCB.InitializeProgressDialog
title: INamespaceWalkCB::InitializeProgressDialog
author: windows-sdk-content
description: Initializes the window title and cancel button text of the progress dialog box displayed during the namespace walk.
old-location: shell\INamespaceWalkCB_InitializeProgressDialog.htm
tech.root: shell
ms.assetid: db105026-5639-4e4e-8146-a14cdb84c48e
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: INamespaceWalkCB interface [Windows Shell],InitializeProgressDialog method, INamespaceWalkCB.InitializeProgressDialog, INamespaceWalkCB::InitializeProgressDialog, InitializeProgressDialog, InitializeProgressDialog method [Windows Shell], InitializeProgressDialog method [Windows Shell],INamespaceWalkCB interface, _win32_INamespaceWalkCB_InitializeProgressDialog, shell.INamespaceWalkCB_InitializeProgressDialog, shobjidl_core/INamespaceWalkCB::InitializeProgressDialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - INamespaceWalkCB.InitializeProgressDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INamespaceWalkCB::InitializeProgressDialog


## -description


Initializes the window title and cancel button text of the progress dialog box displayed during the namespace walk.


## -parameters




### -param ppszTitle [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a null-terminated string that contains the title to be used for the dialog box.


### -param ppszCancel [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a null-terminated string that contains the text displayed on the button that cancels the namespace walk.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



