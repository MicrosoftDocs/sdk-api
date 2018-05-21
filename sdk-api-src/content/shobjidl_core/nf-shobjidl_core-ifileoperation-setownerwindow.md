---
UID: NF:shobjidl_core.IFileOperation.SetOwnerWindow
title: IFileOperation::SetOwnerWindow
author: windows-driver-content
description: Sets the parent or owner window for progress and dialog windows.
old-location: shell\IFileOperation_SetOwnerWindow.htm
old-project: shell
ms.assetid: ad3276a5-409d-4a49-ac95-2c2a3eb3b864
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IFileOperation interface [Windows Shell],SetOwnerWindow method, IFileOperation.SetOwnerWindow, IFileOperation::SetOwnerWindow, SetOwnerWindow, SetOwnerWindow method [Windows Shell], SetOwnerWindow method [Windows Shell],IFileOperation interface, _shell_IFileOperation_SetOwnerWindow, shell.IFileOperation_SetOwnerWindow, shobjidl_core/IFileOperation::SetOwnerWindow
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileOperation.SetOwnerWindow
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileOperation::SetOwnerWindow


## -description


Sets the parent or owner window for progress and dialog windows.


## -parameters




### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the owner window of the operation. This window will receive error messages.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



