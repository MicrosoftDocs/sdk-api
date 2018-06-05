---
UID: NF:shobjidl_core.IFileDialogCustomize.SetControlLabel
title: IFileDialogCustomize::SetControlLabel
author: windows-sdk-content
description: Sets the text associated with a control, such as button text or an edit box label.
old-location: shell\IFileDialogCustomize_SetControlLabel.htm
old-project: shell
ms.assetid: 369038ad-999b-425c-bd47-b6a06e5f6939
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],SetControlLabel method, IFileDialogCustomize.SetControlLabel, IFileDialogCustomize::SetControlLabel, SetControlLabel, SetControlLabel method [Windows Shell], SetControlLabel method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_SetControlLabel, shell_IFileDialogCustomize_SetControlLabel, shobjidl_core/IFileDialogCustomize::SetControlLabel
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IFileDialogCustomize.SetControlLabel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::SetControlLabel


## -description


Sets the text associated with a control, such as button text or an edit box label.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the control whose text is to be changed.


### -param pszLabel [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the text as a null-terminated Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Control labels can be changed at any time, including when the dialog is visible.



