---
UID: NN:shlobj_core.IShellFolderView
title: IShellFolderView (shlobj_core.h)
description: Exposes methods that manipulate Shell folder views.
helpviewer_keywords: ["IShellFolderView","IShellFolderView interface [Windows Shell]","IShellFolderView interface [Windows Shell]","described","_shell_IShellFolderView","shell.IShellFolderView","shlobj_core/IShellFolderView"]
old-location: shell\IShellFolderView.htm
tech.root: shell
ms.assetid: e3b0b35f-6707-4e37-8470-31b1d4421d07
ms.date: 12/05/2018
ms.keywords: IShellFolderView, IShellFolderView interface [Windows Shell], IShellFolderView interface [Windows Shell],described, _shell_IShellFolderView, shell.IShellFolderView, shlobj_core/IShellFolderView
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IShellFolderView
 - shlobj_core/IShellFolderView
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shlobj_core.h
api_name:
 - IShellFolderView
---

# IShellFolderView interface


## -description

<p class="CCE_Message">[<b>IShellFolderView</b> is no longer available for use as of Windows 7. Instead, use <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2">IFolderView2</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a>.]

Exposes methods that manipulate Shell folder views.

## -inheritance

The <b>IShellFolderView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellFolderView</b> also has these types of members:

## -remarks

<b>IShellFolderView</b> is supported by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> object that is returned from <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a>.  This object contains a ListView control and some of the methods on <b>IShellFolderView</b> directly manipulate this ListView control.
