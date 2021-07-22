---
UID: NF:shobjidl.ICommDlgBrowser3.OnPreViewCreated
title: ICommDlgBrowser3::OnPreViewCreated (shobjidl.h)
description: Called after a specified preview is created in the IShellView interface.
helpviewer_keywords: ["ICommDlgBrowser3 interface [Windows Shell]","OnPreViewCreated method","ICommDlgBrowser3.OnPreViewCreated","ICommDlgBrowser3::OnPreViewCreated","OnPreViewCreated","OnPreViewCreated method [Windows Shell]","OnPreViewCreated method [Windows Shell]","ICommDlgBrowser3 interface","_shell_ICommDlgBrowser3_OnPreViewCreated","shell.ICommDlgBrowser3_OnPreViewCreated","shobjidl/ICommDlgBrowser3::OnPreViewCreated"]
old-location: shell\ICommDlgBrowser3_OnPreViewCreated.htm
tech.root: shell
ms.assetid: 1506f553-e0b0-4d6b-9d63-15f3a2d38112
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser3 interface [Windows Shell],OnPreViewCreated method, ICommDlgBrowser3.OnPreViewCreated, ICommDlgBrowser3::OnPreViewCreated, OnPreViewCreated, OnPreViewCreated method [Windows Shell], OnPreViewCreated method [Windows Shell],ICommDlgBrowser3 interface, _shell_ICommDlgBrowser3_OnPreViewCreated, shell.ICommDlgBrowser3_OnPreViewCreated, shobjidl/ICommDlgBrowser3::OnPreViewCreated
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
 - ICommDlgBrowser3::OnPreViewCreated
 - shobjidl/ICommDlgBrowser3::OnPreViewCreated
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
 - ICommDlgBrowser3.OnPreViewCreated
---

# ICommDlgBrowser3::OnPreViewCreated


## -description

Called after a specified preview is created in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

## -parameters

### -param ppshv [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface of the hosted view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.