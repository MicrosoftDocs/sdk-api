---
UID: NF:shobjidl_core.IShellItem2.GetString
title: IShellItem2::GetString (shobjidl_core.h)
description: Gets the string value of a specified property key.
helpviewer_keywords: ["GetString","GetString method [Windows Shell]","GetString method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetString method","IShellItem2.GetString","IShellItem2::GetString","_shell_IShellItem2_GetString","shell.IShellItem2_GetString","shobjidl_core/IShellItem2::GetString"]
old-location: shell\IShellItem2_GetString.htm
tech.root: shell
ms.assetid: 912b3653-340b-4186-b652-53d958534c1d
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Windows Shell], GetString method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetString method, IShellItem2.GetString, IShellItem2::GetString, _shell_IShellItem2_GetString, shell.IShellItem2_GetString, shobjidl_core/IShellItem2::GetString
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
 - IShellItem2::GetString
 - shobjidl_core/IShellItem2::GetString
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
 - IShellItem2.GetString
---

# IShellItem2::GetString


## -description

Gets the string value of a specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param ppsz [out]

Type: <b>LPWSTR*</b>

A pointer to a Unicode string value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.