---
UID: NF:shobjidl_core.IFileDialog.SetFileNameLabel
title: IFileDialog::SetFileNameLabel
author: windows-sdk-content
description: Sets the text of the label next to the file name edit box.
old-location: shell\IFileDialog_SetFileNameLabel.htm
old-project: shell
ms.assetid: 4dc456c4-e06a-4bbf-b7c3-a6f93b46a044
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IFileDialog interface [Windows Shell],SetFileNameLabel method, IFileDialog.SetFileNameLabel, IFileDialog::SetFileNameLabel, SetFileNameLabel, SetFileNameLabel method [Windows Shell], SetFileNameLabel method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetFileNameLabel, shell_IFileDialog_SetFileNameLabel, shobjidl_core/IFileDialog::SetFileNameLabel
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
 - IFileDialog.SetFileNameLabel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog::SetFileNameLabel


## -description


Sets the text of the label next to the file name edit box.


## -parameters




### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the label text.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



