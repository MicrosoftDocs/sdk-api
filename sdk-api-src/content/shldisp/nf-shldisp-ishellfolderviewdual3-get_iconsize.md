---
UID: NF:shldisp.IShellFolderViewDual3.get_IconSize
title: IShellFolderViewDual3::get_IconSize (shldisp.h)
description: Gets the icon size setting for the current folder.
helpviewer_keywords: ["IShellFolderViewDual3 interface [Windows Shell]","get_IconSize method","IShellFolderViewDual3.get_IconSize","IShellFolderViewDual3::get_IconSize","_shell_IShellFolderViewDual3_get_IconSize","get_IconSize","get_IconSize method [Windows Shell]","get_IconSize method [Windows Shell]","IShellFolderViewDual3 interface","shell.IShellFolderViewDual3_get_IconSize","shldisp/IShellFolderViewDual3::get_IconSize"]
old-location: shell\IShellFolderViewDual3_get_IconSize.htm
tech.root: shell
ms.assetid: 005c440f-2340-4965-b717-5aa0f4e5142f
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual3 interface [Windows Shell],get_IconSize method, IShellFolderViewDual3.get_IconSize, IShellFolderViewDual3::get_IconSize, _shell_IShellFolderViewDual3_get_IconSize, get_IconSize, get_IconSize method [Windows Shell], get_IconSize method [Windows Shell],IShellFolderViewDual3 interface, shell.IShellFolderViewDual3_get_IconSize, shldisp/IShellFolderViewDual3::get_IconSize
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
 - IShellFolderViewDual3::get_IconSize
 - shldisp/IShellFolderViewDual3::get_IconSize
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
 - IShellFolderViewDual3.get_IconSize
---

# IShellFolderViewDual3::get_IconSize


## -description

Gets the icon size setting for the current folder.

## -parameters

### -param piIconSize [out]

Type: <b>int*</b>

When this method returns, contains a pointer to the icon size value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

