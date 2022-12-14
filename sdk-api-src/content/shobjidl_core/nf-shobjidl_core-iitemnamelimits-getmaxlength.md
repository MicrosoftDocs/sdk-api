---
UID: NF:shobjidl_core.IItemNameLimits.GetMaxLength
title: IItemNameLimits::GetMaxLength (shobjidl_core.h)
description: Returns the maximum number of characters allowed for a particular name in the namespace under which it is called.
helpviewer_keywords: ["GetMaxLength","GetMaxLength method [Windows Shell]","GetMaxLength method [Windows Shell]","IItemNameLimits interface","IItemNameLimits interface [Windows Shell]","GetMaxLength method","IItemNameLimits.GetMaxLength","IItemNameLimits::GetMaxLength","_shell_IItemNameLimits_GetMaxLength","shell.IItemNameLimits_GetMaxLength","shobjidl_core/IItemNameLimits::GetMaxLength"]
old-location: shell\IItemNameLimits_GetMaxLength.htm
tech.root: shell
ms.assetid: 4bf27218-8ad2-4268-a2e0-1ba36b0db4a3
ms.date: 12/05/2018
ms.keywords: GetMaxLength, GetMaxLength method [Windows Shell], GetMaxLength method [Windows Shell],IItemNameLimits interface, IItemNameLimits interface [Windows Shell],GetMaxLength method, IItemNameLimits.GetMaxLength, IItemNameLimits::GetMaxLength, _shell_IItemNameLimits_GetMaxLength, shell.IItemNameLimits_GetMaxLength, shobjidl_core/IItemNameLimits::GetMaxLength
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IItemNameLimits::GetMaxLength
 - shobjidl_core/IItemNameLimits::GetMaxLength
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
 - IItemNameLimits.GetMaxLength
---

# IItemNameLimits::GetMaxLength


## -description

Returns the maximum number of characters allowed for a particular name in the namespace under which it is called.

## -parameters

### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to a string containing a name.

### -param piMaxNameLen [out]

Type: <b>int*</b>

A pointer to the maximum number of characters which can be used in the name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

