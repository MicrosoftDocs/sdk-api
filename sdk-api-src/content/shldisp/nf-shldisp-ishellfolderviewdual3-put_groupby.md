---
UID: NF:shldisp.IShellFolderViewDual3.put_GroupBy
title: IShellFolderViewDual3::put_GroupBy (shldisp.h)
description: Sets the column used in grouping the folder view.
helpviewer_keywords: ["IShellFolderViewDual3 interface [Windows Shell]","put_GroupBy method","IShellFolderViewDual3.put_GroupBy","IShellFolderViewDual3::put_GroupBy","_shell_IShellFolderViewDual3_put_GroupBy","put_GroupBy","put_GroupBy method [Windows Shell]","put_GroupBy method [Windows Shell]","IShellFolderViewDual3 interface","shell.IShellFolderViewDual3_put_GroupBy","shldisp/IShellFolderViewDual3::put_GroupBy"]
old-location: shell\IShellFolderViewDual3_put_GroupBy.htm
tech.root: shell
ms.assetid: 32c23b6f-7c6f-432c-9f0e-11de8608e546
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],put_GroupBy method, IShellFolderViewDual3.put_GroupBy, IShellFolderViewDual3::put_GroupBy, _shell_IShellFolderViewDual3_put_GroupBy, put_GroupBy, put_GroupBy method [Windows Shell], put_GroupBy method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_put_GroupBy, shldisp/IShellFolderViewDual3::put_GroupBy
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
 - IShellFolderViewDual3::put_GroupBy
 - shldisp/IShellFolderViewDual3::put_GroupBy
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
 - IShellFolderViewDual3.put_GroupBy
---

# IShellFolderViewDual3::put_GroupBy


## -description

Sets the column used in grouping the folder view.

## -parameters

### -param bstrGroupBy [in]

Type: <b><a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a></b>

A <b>BSTR</b> that contains the column name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.