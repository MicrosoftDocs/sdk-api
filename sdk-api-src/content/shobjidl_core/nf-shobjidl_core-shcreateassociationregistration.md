---
UID: NF:shobjidl_core.SHCreateAssociationRegistration
title: SHCreateAssociationRegistration function (shobjidl_core.h)
description: Creates an IApplicationAssociationRegistration object based on the stock implementation of the interface provided by Windows.
helpviewer_keywords: ["SHCreateAssociationRegistration","SHCreateAssociationRegistration function [Windows Shell]","_shell_SHCreateAssociationRegistration","shell.SHCreateAssociationRegistration","shobjidl_core/SHCreateAssociationRegistration"]
old-location: shell\SHCreateAssociationRegistration.htm
tech.root: shell
ms.assetid: 7998f49d-2515-4c77-991e-62c0fefa43df
ms.date: 12/05/2018
ms.keywords: SHCreateAssociationRegistration, SHCreateAssociationRegistration function [Windows Shell], _shell_SHCreateAssociationRegistration, shell.SHCreateAssociationRegistration, shobjidl_core/SHCreateAssociationRegistration
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.Lib
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreateAssociationRegistration
 - shobjidl_core/SHCreateAssociationRegistration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHCreateAssociationRegistration
req.apiset: ext-ms-win-shell-shell32-l1-2-0 (introduced in Windows 8.1)
---

# SHCreateAssociationRegistration function


## -description

Creates an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a> object based on the stock implementation of the interface provided by Windows.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the requested interface.

### -param ppv [out]

Type: <b>void**</b>

When this function returns, contains the address of a pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration">IApplicationAssociationRegistration</a> object.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
