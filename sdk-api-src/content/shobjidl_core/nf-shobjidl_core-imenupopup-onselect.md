---
UID: NF:shobjidl_core.IMenuPopup.OnSelect
title: IMenuPopup::OnSelect (shobjidl_core.h)
description: Handles selection notifications.
helpviewer_keywords: ["IMenuPopup interface [Windows Shell]","OnSelect method","IMenuPopup.OnSelect","IMenuPopup::OnSelect","MPOS_CANCELLEVEL","MPOS_CHILDTRACKING","MPOS_EXECUTE","MPOS_FULLCANCEL","MPOS_SELECTLEFT","MPOS_SELECTRIGHT","OnSelect","OnSelect method [Windows Shell]","OnSelect method [Windows Shell]","IMenuPopup interface","_win32_IMenuPopup_OnSelect","shell.IMenuPopup_OnSelect","shobjidl_core/IMenuPopup::OnSelect"]
old-location: shell\IMenuPopup_OnSelect.htm
tech.root: shell
ms.assetid: 972e8a08-e1ce-4bd2-b602-20b7b1acb71f
ms.date: 12/05/2018
ms.keywords: IMenuPopup interface [Windows Shell],OnSelect method, IMenuPopup.OnSelect, IMenuPopup::OnSelect, MPOS_CANCELLEVEL, MPOS_CHILDTRACKING, MPOS_EXECUTE, MPOS_FULLCANCEL, MPOS_SELECTLEFT, MPOS_SELECTRIGHT, OnSelect, OnSelect method [Windows Shell], OnSelect method [Windows Shell],IMenuPopup interface, _win32_IMenuPopup_OnSelect, shell.IMenuPopup_OnSelect, shobjidl_core/IMenuPopup::OnSelect
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMenuPopup::OnSelect
 - shobjidl_core/IMenuPopup::OnSelect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IMenuPopup.OnSelect
---

# IMenuPopup::OnSelect


## -description

Handles selection notifications.

## -parameters

### -param dwSelectType

Type: <b>DWORD</b>

This parameter can be any of the following values.



#### MPOS_EXECUTE

Execute the selected menu item.



#### MPOS_FULLCANCEL

Cancel the entire menu.



#### MPOS_CANCELLEVEL

Cancel the current cascaded menu.



#### MPOS_SELECTLEFT

Select the item to the left of the current selection.



#### MPOS_SELECTRIGHT

Select the item to the right of the current selection.



#### MPOS_CHILDTRACKING

The child of the current selection receives a tracking selection. In other words, the mouse moves over the child of the current selection.

## -returns

Type: <b>HRESULT</b>

Always returns S_OK.

