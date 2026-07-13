---
UID: NF:shobjidl_core.IExplorerBrowser.Unadvise
title: IExplorerBrowser::Unadvise (shobjidl_core.h)
description: Terminates an advisory connection. (IExplorerBrowser.Unadvise)
helpviewer_keywords: ["IExplorerBrowser interface [Windows Shell]","Unadvise method","IExplorerBrowser.Unadvise","IExplorerBrowser::Unadvise","Unadvise","Unadvise method [Windows Shell]","Unadvise method [Windows Shell]","IExplorerBrowser interface","_shell_IExplorerBrowser_Unadvise","shell.IExplorerBrowser_Unadvise","shobjidl_core/IExplorerBrowser::Unadvise"]
old-location: shell\IExplorerBrowser_Unadvise.htm
tech.root: shell
ms.assetid: a9b6b971-5676-4ceb-ab48-2350a1715b82
ms.date: 12/05/2018
ms.keywords: IExplorerBrowser interface [Windows Shell],Unadvise method, IExplorerBrowser.Unadvise, IExplorerBrowser::Unadvise, Unadvise, Unadvise method [Windows Shell], Unadvise method [Windows Shell],IExplorerBrowser interface, _shell_IExplorerBrowser_Unadvise, shell.IExplorerBrowser_Unadvise, shobjidl_core/IExplorerBrowser::Unadvise
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
 - IExplorerBrowser::Unadvise
 - shobjidl_core/IExplorerBrowser::Unadvise
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
 - IExplorerBrowser.Unadvise
---

# IExplorerBrowser::Unadvise


## -description

Terminates an advisory connection.

## -parameters

### -param dwCookie [in]

Type: <b>DWORD</b>

A connection token previously returned from <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-advise">IExplorerBrowser::Advise</a>. Identifies the connection to be terminated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Terminates an advisory connection previously established through method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-advise">IExplorerBrowser::Advise</a>. The <i>dwCookie</i> parameter identifies the connection to terminate. Failure to call  <b>IExplorerBrowser::Unadvise</b>, may result in a memory leak.
