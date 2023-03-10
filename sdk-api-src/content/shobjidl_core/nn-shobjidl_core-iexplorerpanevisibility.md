---
UID: NN:shobjidl_core.IExplorerPaneVisibility
title: IExplorerPaneVisibility (shobjidl_core.h)
description: Used in Windows Explorer by an IShellFolder implementation to give suggestions to the view about what panes are visible.
helpviewer_keywords: ["IExplorerPaneVisibility","IExplorerPaneVisibility interface [Windows Shell]","IExplorerPaneVisibility interface [Windows Shell]","described","_shell_IExplorerPaneVisibility","shell.IExplorerPaneVisibility","shobjidl_core/IExplorerPaneVisibility"]
old-location: shell\IExplorerPaneVisibility.htm
tech.root: shell
ms.assetid: b940adc2-dfef-49c5-b86c-d0da83db0aad
ms.date: 12/05/2018
ms.keywords: IExplorerPaneVisibility, IExplorerPaneVisibility interface [Windows Shell], IExplorerPaneVisibility interface [Windows Shell],described, _shell_IExplorerPaneVisibility, shell.IExplorerPaneVisibility, shobjidl_core/IExplorerPaneVisibility
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
 - IExplorerPaneVisibility
 - shobjidl_core/IExplorerPaneVisibility
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
 - IExplorerPaneVisibility
---

# IExplorerPaneVisibility interface


## -description

Used in Windows Explorer by an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementation to give suggestions to the view about what panes are visible. Additionally, an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser">IExplorerBrowser</a> host can use this interface to provide information about pane visibility. The host should implement <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> with <b>SID_ExplorerPaneVisibility</b> as the service ID. The host must be in the site chain.

            

The <b>IExplorerPaneVisibility</b> implementation is retrieved from the Shell folder. The Shell folder, in turn, is retrieved from the view. A namespace extension can elect to provide a custom view (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>) rather than using the system folder view object (DefView). In that case, the <b>IShellView</b> implementation must include an implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder">IFolderView::GetFolder</a> to return the <b>IExplorerPaneVisibility</b> object.

A namespace extension can provide a custom view by implementing <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> itself rather than using the system folder view object (DefView). In that case, the <b>IShellView</b> implementation must include an implementation of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder">IFolderView::GetFolder</a> to make use of <b>IExplorerPaneVisibility</b> .

## -inheritance

The <b>IExplorerPaneVisibility</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExplorerPaneVisibility</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview">SHCreateShellFolderView</a>
