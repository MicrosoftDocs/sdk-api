---
UID: NF:shobjidl_core.IFileDialog.SetTitle
title: IFileDialog::SetTitle
author: windows-sdk-content
description: Sets the title of the dialog.
old-location: shell\IFileDialog_SetTitle.htm
old-project: shell
ms.assetid: 9ae3d226-e825-443a-a2b0-4b5bb07fc9f7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IFileDialog interface [Windows Shell],SetTitle method, IFileDialog.SetTitle, IFileDialog::SetTitle, SetTitle, SetTitle method [Windows Shell], SetTitle method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetTitle, shell_IFileDialog_SetTitle, shobjidl_core/IFileDialog::SetTitle
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
 - IFileDialog.SetTitle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::SetTitle


## -description


Sets the title of the dialog.


## -parameters




### -param pszTitle [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the title text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



