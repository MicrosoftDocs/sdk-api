---
UID: NF:shobjidl_core.IActionProgress.ResetCancel
title: IActionProgress::ResetCancel (shobjidl_core.h)
description: Resets progress dialog after a cancellation has been completed.
helpviewer_keywords: ["IActionProgress interface [Windows Shell]","ResetCancel method","IActionProgress.ResetCancel","IActionProgress::ResetCancel","ResetCancel","ResetCancel method [Windows Shell]","ResetCancel method [Windows Shell]","IActionProgress interface","shell.IActionProgress_ResetCancel","shell_IActionProgress_ResetCancel","shobjidl_core/IActionProgress::ResetCancel"]
old-location: shell\IActionProgress_ResetCancel.htm
tech.root: shell
ms.assetid: 28a2ee51-0a7a-4802-be55-f111be3a4d2d
ms.date: 12/05/2018
ms.keywords: IActionProgress interface [Windows Shell],ResetCancel method, IActionProgress.ResetCancel, IActionProgress::ResetCancel, ResetCancel, ResetCancel method [Windows Shell], ResetCancel method [Windows Shell],IActionProgress interface, shell.IActionProgress_ResetCancel, shell_IActionProgress_ResetCancel, shobjidl_core/IActionProgress::ResetCancel
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shobjidl.idl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActionProgress::ResetCancel
 - shobjidl_core/IActionProgress::ResetCancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.idl
api_name:
 - IActionProgress.ResetCancel
---

# IActionProgress::ResetCancel


## -description

Resets progress dialog after a cancellation has been completed.



## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.

## -remarks

This method is called when a cancellation has been completed. User input should typically be limited for cancellations of actions that involve large calculations or file operations. This method may be used by calling applications to notify a progress UI that the cancellation has been completed and the UI should return control to the user.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-querycancel">IActionProgress::QueryCancel</a>
