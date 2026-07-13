---
UID: NF:shobjidl_core.IFileDialog.ClearClientData
title: IFileDialog::ClearClientData (shobjidl_core.h)
description: Instructs the dialog to clear all persisted state information.
helpviewer_keywords: ["ClearClientData","ClearClientData method [Windows Shell]","ClearClientData method [Windows Shell]","IFileDialog interface","IFileDialog interface [Windows Shell]","ClearClientData method","IFileDialog.ClearClientData","IFileDialog::ClearClientData","shell.IFileDialog_ClearClientData","shell_IFileDialog_ClearClientData","shobjidl_core/IFileDialog::ClearClientData"]
old-location: shell\IFileDialog_ClearClientData.htm
tech.root: shell
ms.assetid: bedb6fc8-7db7-4d29-a223-a9997b57c8a3
ms.date: 12/05/2018
ms.keywords: ClearClientData, ClearClientData method [Windows Shell], ClearClientData method [Windows Shell],IFileDialog interface, IFileDialog interface [Windows Shell],ClearClientData method, IFileDialog.ClearClientData, IFileDialog::ClearClientData, shell.IFileDialog_ClearClientData, shell_IFileDialog_ClearClientData, shobjidl_core/IFileDialog::ClearClientData
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
 - IFileDialog::ClearClientData
 - shobjidl_core/IFileDialog::ClearClientData
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
 - IFileDialog.ClearClientData
---

# IFileDialog::ClearClientData


## -description

Instructs the dialog to clear all persisted state information.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Persisted information can be associated with an application or a GUID. If a GUID was set by using <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid">IFileDialog::SetClientGuid</a>, that GUID is used to clear persisted information.
