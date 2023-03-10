---
UID: NF:shobjidl_core.IExplorerBrowser.Initialize
title: IExplorerBrowser::Initialize (shobjidl_core.h)
description: Prepares the browser to be navigated.
helpviewer_keywords: ["IExplorerBrowser interface [Windows Shell]","Initialize method","IExplorerBrowser.Initialize","IExplorerBrowser::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IExplorerBrowser interface","_shell_IExplorerBrowser_Initialize","shell.IExplorerBrowser_Initialize","shobjidl_core/IExplorerBrowser::Initialize"]
old-location: shell\IExplorerBrowser_Initialize.htm
tech.root: shell
ms.assetid: 4b86646a-a20c-4bb5-a4c8-5c2e11e18862
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],Initialize method, IExplorerBrowser.Initialize, IExplorerBrowser::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_Initialize, shell.IExplorerBrowser_Initialize, shobjidl_core/IExplorerBrowser::Initialize
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
 - IExplorerBrowser::Initialize
 - shobjidl_core/IExplorerBrowser::Initialize
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
 - IExplorerBrowser.Initialize
---

# IExplorerBrowser::Initialize


## -description

Prepares the browser to be navigated.

## -parameters

### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the owner window or control.

### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> that contains the coordinates of the bounding rectangle that the browser will occupy. The coordinates are relative to <i>hwndParent</i>.

### -param pfs [in]

Type: <b>const <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a>*</b>

A pointer to a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure that determines how the folder will be displayed in the view. If this parameter is <b>NULL</b>, then you must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setfoldersettings">IExplorerBrowser::SetFolderSettings</a>; otherwise, the default view settings for the folder are used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After calling the <b>Initialize</b> method, it is the responsibility of the caller to call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-destroy">Destroy</a> method to destroy the browser and free any memory and windowed resources associated with the browser.