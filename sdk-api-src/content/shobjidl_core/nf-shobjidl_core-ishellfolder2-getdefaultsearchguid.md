---
UID: NF:shobjidl_core.IShellFolder2.GetDefaultSearchGUID
title: IShellFolder2::GetDefaultSearchGUID (shobjidl_core.h)
description: Returns the globally unique identifier (GUID) of the default search object for the folder.
helpviewer_keywords: ["GetDefaultSearchGUID","GetDefaultSearchGUID method [Windows Shell]","GetDefaultSearchGUID method [Windows Shell]","IShellFolder2 interface","IShellFolder2 interface [Windows Shell]","GetDefaultSearchGUID method","IShellFolder2.GetDefaultSearchGUID","IShellFolder2::GetDefaultSearchGUID","_win32_IShellFolder2_GetDefaultSearchGUID","shell.IShellFolder2_GetDefaultSearchGUID","shobjidl_core/IShellFolder2::GetDefaultSearchGUID"]
old-location: shell\IShellFolder2_GetDefaultSearchGUID.htm
tech.root: shell
ms.assetid: 20acd646-6cb7-420e-84b3-2f9b385a349c
ms.date: 12/05/2018
ms.keywords: GetDefaultSearchGUID, GetDefaultSearchGUID method [Windows Shell], GetDefaultSearchGUID method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],GetDefaultSearchGUID method, IShellFolder2.GetDefaultSearchGUID, IShellFolder2::GetDefaultSearchGUID, _win32_IShellFolder2_GetDefaultSearchGUID, shell.IShellFolder2_GetDefaultSearchGUID, shobjidl_core/IShellFolder2::GetDefaultSearchGUID
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolder2::GetDefaultSearchGUID
 - shobjidl_core/IShellFolder2::GetDefaultSearchGUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellFolder2.GetDefaultSearchGUID
---

# IShellFolder2::GetDefaultSearchGUID


## -description

Returns the globally unique identifier (GUID) of the default search object for the folder.

## -parameters

### -param pguid [out]

Type: <b>GUID*</b>

The GUID of the default search object.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error value otherwise.

