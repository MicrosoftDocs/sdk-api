---
UID: NF:shobjidl_core.IOperationsProgressDialog.SetMode
title: IOperationsProgressDialog::SetMode (shobjidl_core.h)
description: Sets progress dialog operations mode.
helpviewer_keywords: ["IOperationsProgressDialog interface [Windows Shell]","SetMode method","IOperationsProgressDialog.SetMode","IOperationsProgressDialog::SetMode","PDM_DEFAULT","PDM_ERRORSBLOCKING","PDM_INDETERMINATE","PDM_PREFLIGHT","PDM_RUN","PDM_UNDOING","SetMode","SetMode method [Windows Shell]","SetMode method [Windows Shell]","IOperationsProgressDialog interface","_shell_IOperationsProgressDialog_SetMode","shell.IOperationsProgressDialog_SetMode","shobjidl_core/IOperationsProgressDialog::SetMode"]
old-location: shell\IOperationsProgressDialog_SetMode.htm
tech.root: shell
ms.assetid: ec731281-c0af-4cf6-aa63-d80a80a18c15
ms.date: 12/05/2018
ms.keywords: IOperationsProgressDialog interface [Windows Shell],SetMode method, IOperationsProgressDialog.SetMode, IOperationsProgressDialog::SetMode, PDM_DEFAULT, PDM_ERRORSBLOCKING, PDM_INDETERMINATE, PDM_PREFLIGHT, PDM_RUN, PDM_UNDOING, SetMode, SetMode method [Windows Shell], SetMode method [Windows Shell],IOperationsProgressDialog interface, _shell_IOperationsProgressDialog_SetMode, shell.IOperationsProgressDialog_SetMode, shobjidl_core/IOperationsProgressDialog::SetMode
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
 - IOperationsProgressDialog::SetMode
 - shobjidl_core/IOperationsProgressDialog::SetMode
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
 - IOperationsProgressDialog.SetMode
---

# IOperationsProgressDialog::SetMode


## -description

Sets progress dialog operations mode.

## -parameters

### -param mode [in]

Type: <b>PDMODE</b>

Specifies the operation mode. The following are valid values.



#### PDM_DEFAULT

0x00000000. Use the default progress dialog operations mode.



#### PDM_RUN

0x00000001. The operation is running.



#### PDM_PREFLIGHT

0x00000002. The operation is gathering data before it begins, such as calculating the predicted operation time.



#### PDM_UNDOING

0x00000004. The operation is rolling back due to an Undo command from the user.



#### PDM_ERRORSBLOCKING

0x00000008. Error dialogs are blocking progress from continuing.



#### PDM_INDETERMINATE

0x00000010. The length of the operation is indeterminate. Do not show a timer and display the progress bar in marquee mode.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

