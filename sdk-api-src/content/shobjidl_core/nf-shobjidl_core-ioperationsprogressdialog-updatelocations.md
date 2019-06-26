---
UID: NF:shobjidl_core.IOperationsProgressDialog.UpdateLocations
title: IOperationsProgressDialog::UpdateLocations (shobjidl_core.h)
author: windows-sdk-content
description: Called to specify the text elements stating the source and target in the current progress dialog.
old-location: shell\IOperationsProgressDialog_UpdateLocations.htm
tech.root: shell
ms.assetid: df07833a-691c-4d93-a85e-8d21dd04ee64
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOperationsProgressDialog interface [Windows Shell],UpdateLocations method, IOperationsProgressDialog.UpdateLocations, IOperationsProgressDialog::UpdateLocations, UpdateLocations, UpdateLocations method [Windows Shell], UpdateLocations method [Windows Shell],IOperationsProgressDialog interface, _shell_IOperationsProgressDialog_UpdateLocations, shell.IOperationsProgressDialog_UpdateLocations, shobjidl_core/IOperationsProgressDialog::UpdateLocations
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IOperationsProgressDialog.UpdateLocations"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOperationsProgressDialog.UpdateLocations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOperationsProgressDialog::UpdateLocations


## -description


Called to specify the text elements stating the source and target in the current progress dialog.


## -parameters




### -param psiSource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the source Shell item.


### -param psiTarget [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the target Shell item.


### -param psiItem [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that represents the item currently being operated on by the operation engine. This parameter is only used in Windows 7 and later. In earlier versions, this parameter should be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



