---
UID: NF:shobjidl_core.IFileDialogCustomize.GetSelectedControlItem
title: IFileDialogCustomize::GetSelectedControlItem
author: windows-sdk-content
description: Gets a particular item from specified container controls in the dialog.
old-location: shell\IFileDialogCustomize_GetSelectedControlItem.htm
old-project: shell
ms.assetid: 1dd33779-071f-484e-9d89-1cc64ea03293
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: GetSelectedControlItem, GetSelectedControlItem method [Windows Shell], GetSelectedControlItem method [Windows Shell],IFileDialogCustomize interface, IFileDialogCustomize interface [Windows Shell],GetSelectedControlItem method, IFileDialogCustomize.GetSelectedControlItem, IFileDialogCustomize::GetSelectedControlItem, shell.IFileDialogCustomize_GetSelectedControlItem, shell_IFileDialogCustomize_GetSelectedControlItem, shobjidl_core/IFileDialogCustomize::GetSelectedControlItem
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
 - IFileDialogCustomize.GetSelectedControlItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::GetSelectedControlItem


## -description


Gets a particular item from specified container controls in the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the container control.


### -param pdwIDItem [out]

Type: <b>DWORD*</b>

 The ID of the item that the user selected in the control.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To determine the user's final choice, this method can be called on option button groups, combo boxes, and drop-down lists on the <b>Open</b> or <b>Save</b> button after the dialog has closed. This method cannot be called on menus.

For option button groups and combo boxes, this method can also be called while the dialog is showing, to determine the current choice.



