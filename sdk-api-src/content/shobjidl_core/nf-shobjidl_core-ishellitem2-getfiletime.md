---
UID: NF:shobjidl_core.IShellItem2.GetFileTime
title: IShellItem2::GetFileTime (shobjidl_core.h)
description: Gets the date and time value of a specified property key.
helpviewer_keywords: ["GetFileTime","GetFileTime method [Windows Shell]","GetFileTime method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetFileTime method","IShellItem2.GetFileTime","IShellItem2::GetFileTime","_shell_IShellItem2_GetFileTime","shell.IShellItem2_GetFileTime","shobjidl_core/IShellItem2::GetFileTime"]
old-location: shell\IShellItem2_GetFileTime.htm
tech.root: shell
ms.assetid: bdd1834d-ce00-45e2-8fe7-825e18e12b96
ms.date: 12/05/2018
ms.keywords: GetFileTime, GetFileTime method [Windows Shell], GetFileTime method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetFileTime method, IShellItem2.GetFileTime, IShellItem2::GetFileTime, _shell_IShellItem2_GetFileTime, shell.IShellItem2_GetFileTime, shobjidl_core/IShellItem2::GetFileTime
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
 - IShellItem2::GetFileTime
 - shobjidl_core/IShellItem2::GetFileTime
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
 - IShellItem2.GetFileTime
---

# IShellItem2::GetFileTime


## -description

Gets the date and time value of a specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pft [out]

Type: <b>FILETIME*</b>

A pointer to a date and time value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.