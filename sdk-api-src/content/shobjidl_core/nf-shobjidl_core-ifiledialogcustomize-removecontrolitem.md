---
UID: NF:shobjidl_core.IFileDialogCustomize.RemoveControlItem
title: IFileDialogCustomize::RemoveControlItem
author: windows-driver-content
description: Removes an item from a container control in the dialog.
old-location: shell\IFileDialogCustomize_RemoveControlItem.htm
old-project: shell
ms.assetid: 190aaeba-817d-421c-a356-157f3ae7d2e1
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IFileDialogCustomize interface [Windows Shell],RemoveControlItem method, IFileDialogCustomize.RemoveControlItem, IFileDialogCustomize::RemoveControlItem, RemoveControlItem, RemoveControlItem method [Windows Shell], RemoveControlItem method [Windows Shell],IFileDialogCustomize interface, shell.IFileDialogCustomize_RemoveControlItem, shell_IFileDialogCustomize_RemoveControlItem, shobjidl_core/IFileDialogCustomize::RemoveControlItem
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
-	IFileDialogCustomize.RemoveControlItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialogCustomize::RemoveControlItem


## -description


Removes an item from a container control in the dialog.


## -parameters




### -param dwIDCtl [in]

Type: <b>DWORD</b>

The ID of the container control from which the item is to be removed.


### -param dwIDItem [in]

Type: <b>DWORD</b>

The ID of the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Container controls include option button groups, combo boxes, drop-down lists on the <b>Open</b> or <b>Save</b> button, and menus.



