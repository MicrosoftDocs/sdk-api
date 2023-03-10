---
UID: NF:shobjidl_core.IExplorerBrowserEvents.OnViewCreated
title: IExplorerBrowserEvents::OnViewCreated (shobjidl_core.h)
description: Notifies clients that the view of the Explorer browser has been created and can be modified.
helpviewer_keywords: ["IExplorerBrowserEvents interface [Windows Shell]","OnViewCreated method","IExplorerBrowserEvents.OnViewCreated","IExplorerBrowserEvents::OnViewCreated","OnViewCreated","OnViewCreated method [Windows Shell]","OnViewCreated method [Windows Shell]","IExplorerBrowserEvents interface","_shell_IExplorerBrowserEvents_OnViewCreated","shell.IExplorerBrowserEvents_OnViewCreated","shobjidl_core/IExplorerBrowserEvents::OnViewCreated"]
old-location: shell\IExplorerBrowserEvents_OnViewCreated.htm
tech.root: shell
ms.assetid: 801d59f5-6e92-4e3c-938a-e94b43b7c6f1
ms.date: 12/05/2018
ms.keywords: IExplorerBrowserEvents interface [Windows Shell],OnViewCreated method, IExplorerBrowserEvents.OnViewCreated, IExplorerBrowserEvents::OnViewCreated, OnViewCreated, OnViewCreated method [Windows Shell], OnViewCreated method [Windows Shell],IExplorerBrowserEvents interface, _shell_IExplorerBrowserEvents_OnViewCreated, shell.IExplorerBrowserEvents_OnViewCreated, shobjidl_core/IExplorerBrowserEvents::OnViewCreated
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
 - IExplorerBrowserEvents::OnViewCreated
 - shobjidl_core/IExplorerBrowserEvents::OnViewCreated
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
 - IExplorerBrowserEvents.OnViewCreated
---

# IExplorerBrowserEvents::OnViewCreated


## -description

Notifies clients that the view of the Explorer browser has been created and can be modified.

## -parameters

### -param psv [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An Explorer browser calls this method to enable the client to perform any modifications to the Explorer browser view before it is shown; for example, to set view modes or folder flags.