---
UID: NF:shobjidl_core.IShellFolder2.MapColumnToSCID
title: IShellFolder2::MapColumnToSCID (shobjidl_core.h)
description: Converts a column to the appropriate property set ID (FMTID) and property ID (PID).
helpviewer_keywords: ["IShellFolder2 interface [Windows Shell]","MapColumnToSCID method","IShellFolder2.MapColumnToSCID","IShellFolder2::MapColumnToSCID","MapColumnToSCID","MapColumnToSCID method [Windows Shell]","MapColumnToSCID method [Windows Shell]","IShellFolder2 interface","_win32_IShellFolder2_MapColumnToSCID","shell.IShellFolder2_MapColumnToSCID","shobjidl_core/IShellFolder2::MapColumnToSCID"]
old-location: shell\IShellFolder2_MapColumnToSCID.htm
tech.root: shell
ms.assetid: 4bd1f9a1-379b-4488-87d3-c7c7dc47c4d1
ms.date: 12/05/2018
ms.keywords: IShellFolder2 interface [Windows Shell],MapColumnToSCID method, IShellFolder2.MapColumnToSCID, IShellFolder2::MapColumnToSCID, MapColumnToSCID, MapColumnToSCID method [Windows Shell], MapColumnToSCID method [Windows Shell],IShellFolder2 interface, _win32_IShellFolder2_MapColumnToSCID, shell.IShellFolder2_MapColumnToSCID, shobjidl_core/IShellFolder2::MapColumnToSCID
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
 - IShellFolder2::MapColumnToSCID
 - shobjidl_core/IShellFolder2::MapColumnToSCID
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
 - IShellFolder2.MapColumnToSCID
---

# IShellFolder2::MapColumnToSCID


## -description

Converts a column to the appropriate property set ID (FMTID) and property ID (PID).

## -parameters

### -param iColumn [in]

Type: <b>UINT</b>

The column ID.

### -param pscid [out]

Type: <b><a href="/windows/desktop/shell/objects">SHCOLUMNID</a>*</b>

A pointer to an <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> structure containing the FMTID and PID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.