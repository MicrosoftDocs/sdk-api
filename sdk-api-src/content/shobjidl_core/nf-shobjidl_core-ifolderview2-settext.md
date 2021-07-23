---
UID: NF:shobjidl_core.IFolderView2.SetText
title: IFolderView2::SetText (shobjidl_core.h)
description: Sets the default text to be used when there are no items in the view.
helpviewer_keywords: ["FVST_EMPTYTEXT","IFolderView2 interface [Windows Shell]","SetText method","IFolderView2.SetText","IFolderView2::SetText","SetText","SetText method [Windows Shell]","SetText method [Windows Shell]","IFolderView2 interface","_shell_IFolderView2_SetText","shell.IFolderView2_SetText","shobjidl_core/IFolderView2::SetText"]
old-location: shell\IFolderView2_SetText.htm
tech.root: shell
ms.assetid: 72528831-ec5d-417e-94dd-7345b5fd7de6
ms.date: 12/05/2018
ms.keywords: FVST_EMPTYTEXT, IFolderView2 interface [Windows Shell],SetText method, IFolderView2.SetText, IFolderView2::SetText, SetText, SetText method [Windows Shell], SetText method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetText, shell.IFolderView2_SetText, shobjidl_core/IFolderView2::SetText
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFolderView2::SetText
 - shobjidl_core/IFolderView2::SetText
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
 - IFolderView2.SetText
---

# IFolderView2::SetText


## -description

Sets the default text to be used when there are no items in the view.

## -parameters

### -param iType [in]

Type: <b>FVTEXTTYPE</b>

This value should be set to the following flag.



#### FVST_EMPTYTEXT

Set the text to display when there are no items in the view.

### -param pwszText [in]

Type: <b>LPCWSTR</b>

A pointer to a Unicode string that contains the text to be used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

