---
UID: NF:shlwapi.AssocCreate
title: AssocCreate function (shlwapi.h)
description: Returns a pointer to an IQueryAssociations object.
helpviewer_keywords: ["AssocCreate","AssocCreate function [Windows Shell]","_win32_AssocCreate","shell.AssocCreate","shlwapi/AssocCreate"]
old-location: shell\AssocCreate.htm
tech.root: shell
ms.assetid: 33099e0e-73e3-4047-804f-765a59e42e3f
ms.date: 12/05/2018
ms.keywords: AssocCreate, AssocCreate function [Windows Shell], _win32_AssocCreate, shell.AssocCreate, shlwapi/AssocCreate
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AssocCreate
 - shlwapi/AssocCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - ext-ms-win-shell-shlwapi-l1-1-2.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - AssocCreate
---

# AssocCreate function


## -description

Returns a pointer to an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> object.

## -parameters

### -param clsid [in]

Type: <b>CLSID</b>

The CLSID of the object that exposes the interface. This parameter must be set to CLSID_QueryAssociations, which is defined in Shlguid.h.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the IID IID_IQueryAssociations, which is defined in Shlguid.h.

### -param ppv [out]

Type: <b>void*</b>

When this method returns, contains the <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

As of Windows Vista, <a href="/windows/desktop/api/shellapi/nf-shellapi-assoccreateforclasses">AssocCreateForClasses</a> is preferred to <b>AssocCreate</b>.