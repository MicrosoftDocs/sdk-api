---
UID: NF:shobjidl.ICommDlgBrowser3.OnColumnClicked
title: ICommDlgBrowser3::OnColumnClicked (shobjidl.h)
description: Called after a specified column is clicked in the IShellView interface.
helpviewer_keywords: ["ICommDlgBrowser3 interface [Windows Shell]","OnColumnClicked method","ICommDlgBrowser3.OnColumnClicked","ICommDlgBrowser3::OnColumnClicked","OnColumnClicked","OnColumnClicked method [Windows Shell]","OnColumnClicked method [Windows Shell]","ICommDlgBrowser3 interface","_shell_ICommDlgBrowser3_OnColumnClicked","shell.ICommDlgBrowser3_OnColumnClicked","shobjidl/ICommDlgBrowser3::OnColumnClicked"]
old-location: shell\ICommDlgBrowser3_OnColumnClicked.htm
tech.root: shell
ms.assetid: 19cd3dc6-14e4-494d-b4d7-2c9d4fd0fe55
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser3 interface [Windows Shell],OnColumnClicked method, ICommDlgBrowser3.OnColumnClicked, ICommDlgBrowser3::OnColumnClicked, OnColumnClicked, OnColumnClicked method [Windows Shell], OnColumnClicked method [Windows Shell],ICommDlgBrowser3 interface, _shell_ICommDlgBrowser3_OnColumnClicked, shell.ICommDlgBrowser3_OnColumnClicked, shobjidl/ICommDlgBrowser3::OnColumnClicked
req.header: shobjidl.h
req.include-header: 
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
 - ICommDlgBrowser3::OnColumnClicked
 - shobjidl/ICommDlgBrowser3::OnColumnClicked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ICommDlgBrowser3.OnColumnClicked
---

# ICommDlgBrowser3::OnColumnClicked


## -description

Called after a specified column is clicked in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

## -parameters

### -param ppshv [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface of the hosted view.

### -param iColumn [in]

Type: <b>int</b>

The index of the column clicked.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.