---
UID: NF:shobjidl_core.IInitializeWithWindow.Initialize
title: IInitializeWithWindow::Initialize (shobjidl_core.h)
description: Specifies an owner window to be used by a Windows Runtime object that is used in a desktop app.
helpviewer_keywords: ["IInitializeWithWindow interface [Windows Shell]","Initialize method","IInitializeWithWindow.Initialize","IInitializeWithWindow::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeWithWindow interface","shell.IInitializeWithWindow_Initialize","shobjidl_core/IInitializeWithWindow::Initialize"]
old-location: shell\IInitializeWithWindow_Initialize.htm
tech.root: shell
ms.assetid: 429E5D12-9ED9-4f4f-A0E6-F95953C9113A
ms.date: 12/05/2018
ms.keywords: IInitializeWithWindow interface [Windows Shell],Initialize method, IInitializeWithWindow.Initialize, IInitializeWithWindow::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithWindow interface, shell.IInitializeWithWindow_Initialize, shobjidl_core/IInitializeWithWindow::Initialize
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IInitializeWithWindow::Initialize
 - shobjidl_core/IInitializeWithWindow::Initialize
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
 - IInitializeWithWindow.Initialize
---

## -description

Specifies an owner window to be used by a Windows Runtime (WinRT) object that is used in a desktop app.

For info and code examples about this method, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c). In addition to the types listed in that topic, [**Shell data object**](/windows/win32/shell/dataobject) is also associated with this API.

## -parameters

### -param hwnd [in]

The handle of the window to be used as the owner window.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

## -see-also

* [IInitializeWithWindow interface](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow)
* [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects)
