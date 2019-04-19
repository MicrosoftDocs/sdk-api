---
UID: NF:shobjidl_core.IFileDialogCustomize.SetEditBoxText
title: IFileDialogCustomize::SetEditBoxText (shobjidl_core.h)
author: windows-sdk-content
description: Sets the text in an edit box control found in the dialog.
old-location: shell\IFileDialogCustomize_SetEditBoxText.htm
tech.root: shell
ms.assetid: e235e82e-65db-4919-bf71-c454673d07fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetEditBoxText method, IFileDialogCustomize.SetEditBoxText, IFileDialogCustomize::SetEditBoxText, SetEditBoxText, SetEditBoxText method [Windows Shell], SetEditBoxText method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetEditBoxText, shell_IFileDialogCustomize_SetEditBoxText, shobjidl_core/IFileDialogCustomize::SetEditBoxText
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialogCustomize.SetEditBoxText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileDialogCustomize::SetEditBoxText


## -description


Sets the text in an edit box control found in the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the edit box.


### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the text as a null-terminated Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



