---
UID: NF:shobjidl_core.IActionProgress.UpdateText
title: IActionProgress::UpdateText (shobjidl_core.h)
description: Called if descriptive text associated with the action will be changed.
helpviewer_keywords: ["IActionProgress interface [Windows Shell]","UpdateText method","IActionProgress.UpdateText","IActionProgress::UpdateText","UpdateText","UpdateText method [Windows Shell]","UpdateText method [Windows Shell]","IActionProgress interface","shell.IActionProgress_UpdateText","shell_IActionProgress_UpdateText","shobjidl_core/IActionProgress::UpdateText"]
old-location: shell\IActionProgress_UpdateText.htm
tech.root: shell
ms.assetid: dfb8a996-89df-4975-ac13-d871598a2787
ms.date: 12/05/2018
ms.keywords: IActionProgress interface [Windows Shell],UpdateText method, IActionProgress.UpdateText, IActionProgress::UpdateText, UpdateText, UpdateText method [Windows Shell], UpdateText method [Windows Shell],IActionProgress interface, shell.IActionProgress_UpdateText, shell_IActionProgress_UpdateText, shobjidl_core/IActionProgress::UpdateText
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
 - IActionProgress::UpdateText
 - shobjidl_core/IActionProgress::UpdateText
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
 - IActionProgress.UpdateText
---

# IActionProgress::UpdateText


## -description

Called if descriptive text associated with the action will be changed.

## -parameters

### -param sptext [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext">SPTEXT</a></b>

A value that specifies the type of text displayed. See <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext">SPTEXT</a> for acceptable values.

### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a wide character string to display.

### -param fMayCompact [in]

Type: <b>BOOL</b>

A value that specifies whether to allow a text string to be compacted to fit the available space on screen.

## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.

## -remarks

The class implementing this method must interpret the value of <i>sptext</i> and <i>fMayCompact</i> in the context of the action being performed and the UI that shows the progress to the user. The value of <i>sptext</i> can be used to differentiate between lines of changeable text. Often, the value of <i>fMayCompact</i> refers to whether the text string can be truncated with an ellipsis (...) in order to conserve screen space.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext">SPTEXT</a>