---
UID: NF:shldisp.IShellFolderViewDual.get_Script
title: IShellFolderViewDual::get_Script (shldisp.h)
description: Gets the scripting object for the view.
helpviewer_keywords: ["IShellFolderViewDual interface [Windows Shell]","get_Script method","IShellFolderViewDual.get_Script","IShellFolderViewDual::get_Script","_shell_IShellFolderViewDual_get_Script","get_Script","get_Script method [Windows Shell]","get_Script method [Windows Shell]","IShellFolderViewDual interface","shell.IShellFolderViewDual_get_Script","shldisp/IShellFolderViewDual::get_Script"]
old-location: shell\IShellFolderViewDual_get_Script.htm
tech.root: shell
ms.assetid: 9d683cda-0fe0-4984-b556-a6dd1223ca4c
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual interface [Windows Shell],get_Script method, IShellFolderViewDual.get_Script, IShellFolderViewDual::get_Script, _shell_IShellFolderViewDual_get_Script, get_Script, get_Script method [Windows Shell], get_Script method [Windows Shell],IShellFolderViewDual interface, shell.IShellFolderViewDual_get_Script, shldisp/IShellFolderViewDual::get_Script
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
 - IShellFolderViewDual::get_Script
 - shldisp/IShellFolderViewDual::get_Script
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
 - IShellFolderViewDual.get_Script
---

# IShellFolderViewDual::get_Script


## -description

Gets the scripting object for the view.

## -parameters

### -param ppDisp [out]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>**</b>

The scripting object for the view. This represents the scripting automation model.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual">IShellFolderViewDual</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>