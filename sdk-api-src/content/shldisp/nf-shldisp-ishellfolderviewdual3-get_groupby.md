---
UID: NF:shldisp.IShellFolderViewDual3.get_GroupBy
title: IShellFolderViewDual3::get_GroupBy (shldisp.h)
description: Gets the column used for grouping the folder view.
helpviewer_keywords: ["IShellFolderViewDual3 interface [Windows Shell]","get_GroupBy method","IShellFolderViewDual3.get_GroupBy","IShellFolderViewDual3::get_GroupBy","_shell_IShellFolderViewDual3_get_GroupBy","get_GroupBy","get_GroupBy method [Windows Shell]","get_GroupBy method [Windows Shell]","IShellFolderViewDual3 interface","shell.IShellFolderViewDual3_get_GroupBy","shldisp/IShellFolderViewDual3::get_GroupBy"]
old-location: shell\IShellFolderViewDual3_get_GroupBy.htm
tech.root: shell
ms.assetid: 144fa908-01d3-43f4-95e6-2aad62c23912
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],get_GroupBy method, IShellFolderViewDual3.get_GroupBy, IShellFolderViewDual3::get_GroupBy, _shell_IShellFolderViewDual3_get_GroupBy, get_GroupBy, get_GroupBy method [Windows Shell], get_GroupBy method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_get_GroupBy, shldisp/IShellFolderViewDual3::get_GroupBy
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
 - IShellFolderViewDual3::get_GroupBy
 - shldisp/IShellFolderViewDual3::get_GroupBy
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
 - IShellFolderViewDual3.get_GroupBy
---

# IShellFolderViewDual3::get_GroupBy


## -description

Gets the column used for grouping the folder view.

## -parameters

### -param pbstrGroupBy [out]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a>*</b>

When this method returns, contains a pointer to the column name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.