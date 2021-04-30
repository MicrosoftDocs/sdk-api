---
UID: NF:shobjidl.IEnumerableView.SetEnumReadyCallback
title: IEnumerableView::SetEnumReadyCallback (shobjidl.h)
description: Sets a callback on the view that is notified when the initial view enumeration is complete.
helpviewer_keywords: ["IEnumerableView interface [Windows Shell]","SetEnumReadyCallback method","IEnumerableView.SetEnumReadyCallback","IEnumerableView::SetEnumReadyCallback","SetEnumReadyCallback","SetEnumReadyCallback method [Windows Shell]","SetEnumReadyCallback method [Windows Shell]","IEnumerableView interface","_shell_IEnumerableView_SetEnumReadyCallback","shell.IEnumerableView_SetEnumReadyCallback","shobjidl/IEnumerableView::SetEnumReadyCallback"]
old-location: shell\IEnumerableView_SetEnumReadyCallback.htm
tech.root: shell
ms.assetid: af824c16-5bbf-4c75-88d0-b76519152360
ms.date: 12/05/2018
ms.keywords: IEnumerableView interface [Windows Shell],SetEnumReadyCallback method, IEnumerableView.SetEnumReadyCallback, IEnumerableView::SetEnumReadyCallback, SetEnumReadyCallback, SetEnumReadyCallback method [Windows Shell], SetEnumReadyCallback method [Windows Shell],IEnumerableView interface, _shell_IEnumerableView_SetEnumReadyCallback, shell.IEnumerableView_SetEnumReadyCallback, shobjidl/IEnumerableView::SetEnumReadyCallback
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
 - IEnumerableView::SetEnumReadyCallback
 - shobjidl/IEnumerableView::SetEnumReadyCallback
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
 - IEnumerableView.SetEnumReadyCallback
---

# IEnumerableView::SetEnumReadyCallback


## -description

Sets a callback on the view that is notified when the initial view enumeration is complete.

## -parameters

### -param percb [in]

Type: <b><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ienumreadycallback">IEnumReadyCallback</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl/nn-shobjidl-ienumreadycallback">IEnumReadyCallback</a> interface.

## -returns

Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.