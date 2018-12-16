---
UID: NF:shobjidl_core.IOperationsProgressDialog.UpdateProgress
title: IOperationsProgressDialog::UpdateProgress
author: windows-sdk-content
description: Updates the current progress dialog, as specified.
old-location: shell\IOperationsProgressDialog_UpdateProgress.htm
tech.root: shell
ms.assetid: 5ff2def3-f320-412c-8f98-bd1a58866d03
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOperationsProgressDialog interface [Windows Shell],UpdateProgress method, IOperationsProgressDialog.UpdateProgress, IOperationsProgressDialog::UpdateProgress, UpdateProgress, UpdateProgress method [Windows Shell], UpdateProgress method [Windows Shell],IOperationsProgressDialog interface, _shell_IOperationsProgressDialog_UpdateProgress, shell.IOperationsProgressDialog_UpdateProgress, shobjidl_core/IOperationsProgressDialog::UpdateProgress
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
 - IOperationsProgressDialog.UpdateProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOperationsProgressDialog::UpdateProgress


## -description


Updates the current progress dialog, as specified.


## -parameters




### -param ullPointsCurrent [in]

Type: <b>ULONGLONG</b>

Current points, used for showing progress in points.


### -param ullPointsTotal [in]

Type: <b>ULONGLONG</b>

Total points, used for showing progress in points.


### -param ullSizeCurrent [in]

Type: <b>ULONGLONG</b>

Current size in bytes, used for showing progress in bytes.


### -param ullSizeTotal [in]

Type: <b>ULONGLONG</b>

Total size in bytes, used for showing progress in bytes.


### -param ullItemsCurrent [in]

Type: <b>ULONGLONG</b>

Current items, used for showing progress in items.


### -param ullItemsTotal [in]

Type: <b>ULONGLONG</b>

Specifies total items, used for showing progress in items.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



