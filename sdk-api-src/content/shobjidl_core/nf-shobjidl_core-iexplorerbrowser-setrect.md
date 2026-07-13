---
UID: NF:shobjidl_core.IExplorerBrowser.SetRect
title: IExplorerBrowser::SetRect (shobjidl_core.h)
description: Sets the size and position of the view windows created by the browser.
helpviewer_keywords: ["IExplorerBrowser interface [Windows Shell]","SetRect method","IExplorerBrowser.SetRect","IExplorerBrowser::SetRect","SetRect","SetRect method [Windows Shell]","SetRect method [Windows Shell]","IExplorerBrowser interface","_shell_IExplorerBrowser_SetRect","shell.IExplorerBrowser_SetRect","shobjidl_core/IExplorerBrowser::SetRect"]
old-location: shell\IExplorerBrowser_SetRect.htm
tech.root: shell
ms.assetid: 392052ea-1053-4f55-96aa-2d64b0ee0390
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],SetRect method, IExplorerBrowser.SetRect, IExplorerBrowser::SetRect, SetRect, SetRect method [Windows Shell], SetRect method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_SetRect, shell.IExplorerBrowser_SetRect, shobjidl_core/IExplorerBrowser::SetRect
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
 - IExplorerBrowser::SetRect
 - shobjidl_core/IExplorerBrowser::SetRect
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
 - IExplorerBrowser.SetRect
---

# IExplorerBrowser::SetRect


## -description

Sets the size and position of the view windows created by the browser.

## -parameters

### -param phdwp [in, out]

Type: <b>HDWP*</b>

A pointer to a <a href="/windows/desktop/api/winuser/nf-winuser-deferwindowpos">DeferWindowPos</a> handle. This parameter can be <b>NULL</b>.

### -param rcBrowser [in]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The coordinates that the browser will occupy.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Coordinates are relative to the <i>hwndParent</i> passed in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-initialize">IExplorerBrowser::Initialize</a>.