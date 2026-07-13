---
UID: NF:shobjidl_core.IShellFolder2.GetDetailsEx
title: IShellFolder2::GetDetailsEx (shobjidl_core.h)
description: Gets detailed information, identified by a property set identifier (FMTID) and a property identifier (PID), on an item in a Shell folder.
helpviewer_keywords: ["GetDetailsEx","GetDetailsEx method [Windows Shell]","GetDetailsEx method [Windows Shell]","IShellFolder2 interface","IShellFolder2 interface [Windows Shell]","GetDetailsEx method","IShellFolder2.GetDetailsEx","IShellFolder2::GetDetailsEx","_win32_IShellFolder2_GetDetailsEx","shell.IShellFolder2_GetDetailsEx","shobjidl_core/IShellFolder2::GetDetailsEx"]
old-location: shell\IShellFolder2_GetDetailsEx.htm
tech.root: shell
ms.assetid: f006828c-980d-4e36-be68-3b3c238cd884
ms.date: 12/05/2018
ms.keywords: GetDetailsEx, GetDetailsEx method [Windows Shell], GetDetailsEx method [Windows Shell],IShellFolder2 interface, IShellFolder2 interface [Windows Shell],GetDetailsEx method, IShellFolder2.GetDetailsEx, IShellFolder2::GetDetailsEx, _win32_IShellFolder2_GetDetailsEx, shell.IShellFolder2_GetDetailsEx, shobjidl_core/IShellFolder2::GetDetailsEx
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
 - IShellFolder2::GetDetailsEx
 - shobjidl_core/IShellFolder2::GetDetailsEx
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
 - IShellFolder2.GetDetailsEx
---

# IShellFolder2::GetDetailsEx


## -description

Gets detailed information, identified by a property set identifier (FMTID) and a property identifier (PID), on an item in a Shell folder.

## -parameters

### -param pidl [in]

Type: <b>PCUITEMID_CHILD</b>

A PIDL of the item, relative to the parent folder. This method accepts only single-level PIDLs. The structure must contain exactly one <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure followed by a terminating zero. This value cannot be <b>NULL</b>.

### -param pscid [in]

Type: <b>const <a href="/windows/desktop/shell/objects">SHCOLUMNID</a>*</b>

A pointer to an <a href="/windows/desktop/shell/objects">SHCOLUMNID</a> structure that identifies the column.

### -param pv [out]

Type: <b>VARIANT*</b>

A pointer to a <b>VARIANT</b> with the requested information. The value is fully typed. The value returned for properties from the property system must conform to the type specified in that property definition's <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> as the <i>legacyType</i> attribute.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is a more robust version of <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof">IShellFolder2::GetDetailsOf</a>. It provides access to the information that is displayed in the Windows Explorer Details view of a Shell folder. The primary difference is that <b>GetDetailsEx</b> allows you to identify the column with an <a href="/windows/desktop/shell/objects">FMTID</a> and PID structure instead of having to first determine the column index.