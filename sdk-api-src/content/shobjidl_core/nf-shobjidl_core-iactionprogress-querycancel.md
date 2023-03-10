---
UID: NF:shobjidl_core.IActionProgress.QueryCancel
title: IActionProgress::QueryCancel (shobjidl_core.h)
description: Provides information about whether the action is being canceled.
helpviewer_keywords: ["IActionProgress interface [Windows Shell]","QueryCancel method","IActionProgress.QueryCancel","IActionProgress::QueryCancel","QueryCancel","QueryCancel method [Windows Shell]","QueryCancel method [Windows Shell]","IActionProgress interface","shell.IActionProgress_QueryCancel","shell_IActionProgress_QueryCancel","shobjidl_core/IActionProgress::QueryCancel"]
old-location: shell\IActionProgress_QueryCancel.htm
tech.root: shell
ms.assetid: a5db4344-c1b4-4e76-9291-46dafc82e88d
ms.date: 12/05/2018
ms.keywords: IActionProgress interface [Windows Shell],QueryCancel method, IActionProgress.QueryCancel, IActionProgress::QueryCancel, QueryCancel, QueryCancel method [Windows Shell], QueryCancel method [Windows Shell],IActionProgress interface, shell.IActionProgress_QueryCancel, shell_IActionProgress_QueryCancel, shobjidl_core/IActionProgress::QueryCancel
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
 - IActionProgress::QueryCancel
 - shobjidl_core/IActionProgress::QueryCancel
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
 - IActionProgress.QueryCancel
---

# IActionProgress::QueryCancel


## -description

Provides information about whether the action is being canceled.

## -parameters

### -param pfCancelled [out]

Type: <b>BOOL*</b>

A reference to a <b>BOOL</b> value that specifies whether the action is being canceled.

## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.

## -remarks

Call this method when a process must know whether an action has been canceled. Implementing this method requires the implementing class to query either an internal or external flag to provide this information, and store the result in the value of <i>pfCancelled</i>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress">IActionProgress</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-resetcancel">IActionProgress::ResetCancel</a>