---
UID: NF:shobjidl_core.IFileDialog.SetClientGuid
title: IFileDialog::SetClientGuid (shobjidl_core.h)
description: Enables a calling application to associate a GUID with a dialog's persisted state.
helpviewer_keywords: ["IFileDialog interface [Windows Shell]","SetClientGuid method","IFileDialog.SetClientGuid","IFileDialog::SetClientGuid","SetClientGuid","SetClientGuid method [Windows Shell]","SetClientGuid method [Windows Shell]","IFileDialog interface","shell.IFileDialog_SetClientGuid","shell_IFileDialog_SetClientGuid","shobjidl_core/IFileDialog::SetClientGuid"]
old-location: shell\IFileDialog_SetClientGuid.htm
tech.root: shell
ms.assetid: 2ab7d8bb-068d-4c5b-b273-68c7fc4f9956
ms.date: 12/05/2018
ms.keywords: IFileDialog interface [Windows Shell],SetClientGuid method, IFileDialog.SetClientGuid, IFileDialog::SetClientGuid, SetClientGuid, SetClientGuid method [Windows Shell], SetClientGuid method [Windows Shell],IFileDialog interface, shell.IFileDialog_SetClientGuid, shell_IFileDialog_SetClientGuid, shobjidl_core/IFileDialog::SetClientGuid
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
 - IFileDialog::SetClientGuid
 - shobjidl_core/IFileDialog::SetClientGuid
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
 - IFileDialog.SetClientGuid
---

# IFileDialog::SetClientGuid


## -description

Enables a calling application to associate a GUID with a dialog's persisted state.

## -parameters

### -param guid [in]

Type: <b>REFGUID</b>

The GUID to associate with this dialog state.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A dialog's state can include factors such as the last visited folder and the position and size of the dialog.

Typically, this state is persisted based on the name of the executable file. By specifying a GUID, an application can have different persisted states for different versions of the dialog within the same application (for example, an import dialog and an open dialog).
            

<b>IFileDialog::SetClientGuid</b> should be called immediately after creation of the dialog object.

