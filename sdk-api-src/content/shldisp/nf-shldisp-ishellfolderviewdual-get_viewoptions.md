---
UID: NF:shldisp.IShellFolderViewDual.get_ViewOptions
title: IShellFolderViewDual::get_ViewOptions (shldisp.h)
description: Gets a set of flags that indicate the current options of the view.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","get_ViewOptions method","IShellFolderViewDual.get_ViewOptions","IShellFolderViewDual::get_ViewOptions","_shell_IShellFolderViewDual_get_ViewOptions","get_ViewOptions","get_ViewOptions method [Windows Shell]","get_ViewOptions method [Windows Shell]","IShellFolderViewDual interface","shell.IShellFolderViewDual_get_ViewOptions","shldisp/IShellFolderViewDual::get_ViewOptions"]
old-location: shell\IShellFolderViewDual_get_ViewOptions.htm
tech.root: shell
ms.assetid: 1ef3a163-bc38-40b2-aa3e-dcd36f87964f
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],get_ViewOptions method, IShellFolderViewDual.get_ViewOptions, IShellFolderViewDual::get_ViewOptions, _shell_IShellFolderViewDual_get_ViewOptions, get_ViewOptions, get_ViewOptions method [Windows Shell], get_ViewOptions method [Windows Shell],IShellFolderViewDual interface, shell.IShellFolderViewDual_get_ViewOptions, shldisp/IShellFolderViewDual::get_ViewOptions
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
 - IShellFolderViewDual::get_ViewOptions
 - shldisp/IShellFolderViewDual::get_ViewOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shldisp.h
api_name:
 - IShellFolderViewDual.get_ViewOptions
---

# IShellFolderViewDual::get_ViewOptions


## -description

Gets a set of flags that indicate the current options of the view.

## -parameters

### -param plViewOptions [out]

Type: <b>long*</b>

The set of flags that indicate the current options of the view.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>