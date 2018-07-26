---
UID: NF:shobjidl_core.IFolderView2.SetText
title: IFolderView2::SetText
author: windows-sdk-content
description: Sets the default text to be used when there are no items in the view.
old-location: shell\IFolderView2_SetText.htm
old-project: shell
ms.assetid: 72528831-ec5d-417e-94dd-7345b5fd7de6
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: FVST_EMPTYTEXT, IFolderView2 interface [Windows Shell],SetText method, IFolderView2.SetText, IFolderView2::SetText, SetText, SetText method [Windows Shell], SetText method [Windows Shell],IFolderView2 interface, _shell_IFolderView2_SetText, shell.IFolderView2_SetText, shobjidl_core/IFolderView2::SetText
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
 - IFolderView2.SetText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



