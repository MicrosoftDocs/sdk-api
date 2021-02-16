---
UID: NF:shobjidl_core.IActionProgress.UpdateProgress
title: IActionProgress::UpdateProgress (shobjidl_core.h)
description: Updates the progress of an action to the UI.
helpviewer_keywords: ["IActionProgress interface [Windows Shell]","UpdateProgress method","IActionProgress.UpdateProgress","IActionProgress::UpdateProgress","UpdateProgress","UpdateProgress method [Windows Shell]","UpdateProgress method [Windows Shell]","IActionProgress interface","shell.IActionProgress_UpdateProgress","shell_IActionProgress_UpdateProgress","shobjidl_core/IActionProgress::UpdateProgress"]
old-location: shell\IActionProgress_UpdateProgress.htm
tech.root: shell
ms.assetid: d9c6fd82-96a2-4021-a6c4-ab61e20eb0d0
ms.date: 12/05/2018
ms.keywords: IActionProgress interface [Windows Shell],UpdateProgress method, IActionProgress.UpdateProgress, IActionProgress::UpdateProgress, UpdateProgress, UpdateProgress method [Windows Shell], UpdateProgress method [Windows Shell],IActionProgress interface, shell.IActionProgress_UpdateProgress, shell_IActionProgress_UpdateProgress, shobjidl_core/IActionProgress::UpdateProgress
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
 - IActionProgress::UpdateProgress
 - shobjidl_core/IActionProgress::UpdateProgress
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
 - IActionProgress.UpdateProgress
---

# IActionProgress::UpdateProgress


## -description

Updates the progress of an action to the UI.

## -parameters

### -param ulCompleted [in]

Type: <b>ULONGLONG</b>

The amount of the action completed.

### -param ulTotal [in]

Type: <b>ULONGLONG</b>

The total amount of the action.

## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.

## -remarks

This method should be called periodically to update the progress of the action. The implementing class may interpret these values in any way desired, although the values of <i>ulCompleted</i> and <i>ulTotal</i> should be interpreted relative to one another to determine a meaningful progress amount. Often, a percentage is desired, in which case the value of <i>ulCompleted</i> should be divided by <i>ulTotal</i>, and the result multiplied by a value of 100.

