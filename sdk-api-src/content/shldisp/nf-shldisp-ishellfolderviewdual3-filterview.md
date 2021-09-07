---
UID: NF:shldisp.IShellFolderViewDual3.FilterView
title: IShellFolderViewDual3::FilterView (shldisp.h)
description: Sets the filter on the contents of the current view.
helpviewer_keywords: ["FilterView","FilterView method [Windows Shell]","FilterView method [Windows Shell]","IShellFolderViewDual3 interface","IShellFolderViewDual3 interface [Windows Shell]","FilterView method","IShellFolderViewDual3.FilterView","IShellFolderViewDual3::FilterView","_shell_IShellFolderViewDual3_FilterView","shell.IShellFolderViewDual3_FilterView","shldisp/IShellFolderViewDual3::FilterView"]
old-location: shell\IShellFolderViewDual3_FilterView.htm
tech.root: shell
ms.assetid: 60808015-317e-469f-aa28-a2c2bfdb16a8
ms.date: 12/05/2018
ms.keywords: FilterView, FilterView method [Windows Shell], FilterView method [Windows Shell],IShellFolderViewDual3 interface, IShellFolderViewDual3 interface [Windows Shell],FilterView method, IShellFolderViewDual3.FilterView, IShellFolderViewDual3::FilterView, _shell_IShellFolderViewDual3_FilterView, shell.IShellFolderViewDual3_FilterView, shldisp/IShellFolderViewDual3::FilterView
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IShellFolderViewDual3::FilterView
 - shldisp/IShellFolderViewDual3::FilterView
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
 - IShellFolderViewDual3.FilterView
---

# IShellFolderViewDual3::FilterView


## -description

Sets the filter on the contents of the current view.

## -parameters

### -param bstrFilterText [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

The BSTR that names the filter view for the current folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.