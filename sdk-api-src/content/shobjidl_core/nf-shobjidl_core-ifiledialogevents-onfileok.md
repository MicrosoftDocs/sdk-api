---
UID: NF:shobjidl_core.IFileDialogEvents.OnFileOk
title: IFileDialogEvents::OnFileOk
author: windows-sdk-content
description: Called just before the dialog is about to return with a result.
old-location: shell\IFileDialogEvents_OnFileOk.htm
old-project: shell
ms.assetid: 81277122-b2fe-40af-85f8-d578925856a1
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IFileDialogEvents interface [Windows Shell],OnFileOk method, IFileDialogEvents.OnFileOk, IFileDialogEvents::OnFileOk, OnFileOk, OnFileOk method [Windows Shell], OnFileOk method [Windows Shell],IFileDialogEvents interface, shell.IFileDialogEvents_OnFileOk, shell_IFileDialogEvents_OnFileOk, shobjidl_core/IFileDialogEvents::OnFileOk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
 - IFileDialogEvents.OnFileOk
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogEvents::OnFileOk


## -description


Called just before the dialog is about to return with a result.


## -parameters




### -param pfd [in]

Type: <b><a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>*</b>

A pointer to the interface that represents the dialog.


## -returns



Type: <b>HRESULT</b>

Implementations should return <b>S_OK</b> to accept the current result in the dialog or <b>S_FALSE</b> to refuse it. In the case of <b>S_FALSE</b>, the dialog should remain open.




## -remarks



When this method is called, the <a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">IFileDialog::GetResult</a> and <a href="https://msdn.microsoft.com/5c710dae-4988-4f19-beb5-2ff9cd11c596">GetResults</a> methods can be called.

The application can use this callback method to perform additional validation before the dialog closes, or to prevent the dialog from closing. If the application prevents the dialog from closing, it should display a UI to indicate a cause. To obtain a parent <b>HWND</b> for the UI, obtain the <a href="https://msdn.microsoft.com/2d0efbae-4a1c-43b1-9021-8d89377f7282">IOleWindow</a> interface through <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IFileDialog::QueryInterface</a> and call <a href="https://msdn.microsoft.com/833adc81-be58-44a1-88f1-9aa28808e67b">IOleWindow::GetWindow</a>.

An application can also use this method to perform all of its work surrounding the opening or saving of files.



