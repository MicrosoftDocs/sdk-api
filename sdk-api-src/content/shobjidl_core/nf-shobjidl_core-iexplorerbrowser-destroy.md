---
UID: NF:shobjidl_core.IExplorerBrowser.Destroy
title: IExplorerBrowser::Destroy (shobjidl_core.h)
description: Destroys the browser.
helpviewer_keywords: ["Destroy","Destroy method [Windows Shell]","Destroy method [Windows Shell]","IExplorerBrowser interface","IExplorerBrowser interface [Windows Shell]","Destroy method","IExplorerBrowser.Destroy","IExplorerBrowser::Destroy","_shell_IExplorerBrowser_Destroy","shell.IExplorerBrowser_Destroy","shobjidl_core/IExplorerBrowser::Destroy"]
old-location: shell\IExplorerBrowser_Destroy.htm
tech.root: shell
ms.assetid: b6fc4aa6-f689-4b3e-a922-f8361d33b6dd
ms.date: 12/05/2018
ms.keywords: Destroy, Destroy method [Windows Shell], Destroy method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],Destroy method, IExplorerBrowser.Destroy, IExplorerBrowser::Destroy, _shell_IExplorerBrowser_Destroy, shell.IExplorerBrowser_Destroy, shobjidl_core/IExplorerBrowser::Destroy
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
 - IExplorerBrowser::Destroy
 - shobjidl_core/IExplorerBrowser::Destroy
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
 - IExplorerBrowser.Destroy
---

# IExplorerBrowser::Destroy


## -description

Destroys the browser.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-initialize">IExplorerBrowser::Initialize</a> was called., then method <b>IExplorerBrowser::Destroy</b> must be called to free resources. Failure to call <b>IExplorerBrowser::Destroy</b> may cause a memory leak.
