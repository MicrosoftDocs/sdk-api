---
UID: NF:shobjidl_core.IShellItem2.GetUInt32
title: IShellItem2::GetUInt32 (shobjidl_core.h)
description: Gets the UInt32 value of a specified property key.
helpviewer_keywords: ["GetUInt32","GetUInt32 method [Windows Shell]","GetUInt32 method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetUInt32 method","IShellItem2.GetUInt32","IShellItem2::GetUInt32","_shell_IShellItem2_GetUInt32","shell.IShellItem2_GetUInt32","shobjidl_core/IShellItem2::GetUInt32"]
old-location: shell\IShellItem2_GetUInt32.htm
tech.root: shell
ms.assetid: 5f9b479f-974f-4fad-87ea-7335d4d5d2e3
ms.date: 12/05/2018
ms.keywords: GetUInt32, GetUInt32 method [Windows Shell], GetUInt32 method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetUInt32 method, IShellItem2.GetUInt32, IShellItem2::GetUInt32, _shell_IShellItem2_GetUInt32, shell.IShellItem2_GetUInt32, shobjidl_core/IShellItem2::GetUInt32
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItem2::GetUInt32
 - shobjidl_core/IShellItem2::GetUInt32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItem2.GetUInt32
---

# IShellItem2::GetUInt32


## -description

Gets the UInt32 value of a specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pui [out]

Type: <b>ULONG*</b>

Receives a pointer to a UInt32 value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.