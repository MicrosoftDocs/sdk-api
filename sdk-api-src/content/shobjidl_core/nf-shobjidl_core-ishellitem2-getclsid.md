---
UID: NF:shobjidl_core.IShellItem2.GetCLSID
title: IShellItem2::GetCLSID (shobjidl_core.h)
description: Gets the class identifier (CLSID) value of specified property key.
helpviewer_keywords: ["GetCLSID","GetCLSID method [Windows Shell]","GetCLSID method [Windows Shell]","IShellItem2 interface","IShellItem2 interface [Windows Shell]","GetCLSID method","IShellItem2.GetCLSID","IShellItem2::GetCLSID","_shell_IShellItem2_GetCLSID","shell.IShellItem2_GetCLSID","shobjidl_core/IShellItem2::GetCLSID"]
old-location: shell\IShellItem2_GetCLSID.htm
tech.root: shell
ms.assetid: 95b0c5fb-db09-4db0-8253-708f2dc2944b
ms.date: 12/05/2018
ms.keywords: GetCLSID, GetCLSID method [Windows Shell], GetCLSID method [Windows Shell],IShellItem2 interface, IShellItem2 interface [Windows Shell],GetCLSID method, IShellItem2.GetCLSID, IShellItem2::GetCLSID, _shell_IShellItem2_GetCLSID, shell.IShellItem2_GetCLSID, shobjidl_core/IShellItem2::GetCLSID
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
 - IShellItem2::GetCLSID
 - shobjidl_core/IShellItem2::GetCLSID
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
 - IShellItem2.GetCLSID
---

# IShellItem2::GetCLSID


## -description

Gets the class identifier (CLSID) value of specified property key.

## -parameters

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure.

### -param pclsid [out]

Type: <b>CLSID*</b>

A pointer to a CLSID value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.