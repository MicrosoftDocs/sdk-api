---
UID: NF:shobjidl_core.IShellItem2.GetBool
title: IShellItem2::GetBool (shobjidl_core.h)
description: Gets the boolean value of a specified property key.
helpviewer_keywords: ["GetBool","GetBool method [Windows Shell]","GetBool method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetBool method","IShellItem2.GetBool","IShellItem2::GetBool","_shell_IShellItem2_GetBool","shell.IShellItem2_GetBool","shobjidl_core/IShellItem2::GetBool"]
old-location: shell\IShellItem2_GetBool.htm
tech.root: shell
ms.assetid: 754d0a7a-a6b4-41ef-8c8f-483539f7d53e
ms.date: 12/05/2018
ms.keywords: GetBool, GetBool method [Windows Shell], GetBool method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetBool method, IShellItem2.GetBool, IShellItem2::GetBool, _shell_IShellItem2_GetBool, shell.IShellItem2_GetBool, shobjidl_core/IShellItem2::GetBool
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
 - IShellItem2::GetBool
 - shobjidl_core/IShellItem2::GetBool
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
 - IShellItem2.GetBool
---

# IShellItem2::GetBool


## -description

Gets the boolean value of a specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pf [out]

Type: <b>BOOL*</b>

A pointer to a boolean value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.