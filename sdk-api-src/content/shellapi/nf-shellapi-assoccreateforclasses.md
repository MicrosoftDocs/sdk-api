---
UID: NF:shellapi.AssocCreateForClasses
title: AssocCreateForClasses function (shellapi.h)
description: Retrieves an object that implements an IQueryAssociations interface.
helpviewer_keywords: ["AssocCreateForClasses","AssocCreateForClasses function [Windows Shell]","_shell_AssocCreateForClasses","shell.AssocCreateForClasses","shellapi/AssocCreateForClasses"]
old-location: shell\AssocCreateForClasses.htm
tech.root: shell
ms.assetid: 43257507-dd5e-4622-8445-c132187fd1e5
ms.date: 12/05/2018
ms.keywords: AssocCreateForClasses, AssocCreateForClasses function [Windows Shell], _shell_AssocCreateForClasses, shell.AssocCreateForClasses, shellapi/AssocCreateForClasses
req.header: shellapi.h
req.include-header: 
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
 - AssocCreateForClasses
 - shellapi/AssocCreateForClasses
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
 - api-ms-win-shell-associations-l1-1-3.dll
 - api-ms-win-shell-associations-l1-1-2.dll
 - api-ms-win-shell-associations-l1-1-1.dll
 - Shell32.dll
 - Windows.Storage.dll
 - API-MS-Win-Shell-Associations-L1-1-0.dll
api_name:
 - AssocCreateForClasses
req.apiset: ext-ms-win-shell-shell32-l1-2-2 (introduced in Windows 10, version 10.0.14393)
---

# AssocCreateForClasses function


## -description

Retrieves an object that implements an <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a> interface.

## -parameters

### -param rgClasses [in]

Type: <b>const <a href="/windows/desktop/api/shellapi/ns-shellapi-associationelement">ASSOCIATIONELEMENT</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/shellapi/ns-shellapi-associationelement">ASSOCIATIONELEMENT</a> structures.

### -param cClasses [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>rgClasses</i>.

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID, normally IID_IQueryAssociations.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is normally <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations">IQueryAssociations</a>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For systems earlier than Windows Vista, use the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate">AssocCreate</a> function.
