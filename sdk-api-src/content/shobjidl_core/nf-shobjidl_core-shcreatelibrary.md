---
UID: NF:shobjidl_core.SHCreateLibrary
title: SHCreateLibrary function (shobjidl_core.h)
description: Creates an IShellLibrary object.
helpviewer_keywords: ["SHCreateLibrary","SHCreateLibrary function [Windows Shell]","_shell_SHCreateLibrary","shell.SHCreateLibrary","shobjidl_core/SHCreateLibrary"]
old-location: shell\SHCreateLibrary.htm
tech.root: shell
ms.assetid: 7e682a2e-5140-49ad-88de-ac681025aca4
ms.date: 12/05/2018
ms.keywords: SHCreateLibrary, SHCreateLibrary function [Windows Shell], _shell_SHCreateLibrary, shell.SHCreateLibrary, shobjidl_core/SHCreateLibrary
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - SHCreateLibrary
 - shobjidl_core/SHCreateLibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHCreateLibrary
---

# SHCreateLibrary function


## -description

Creates an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The IID for <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>. (See usage remarks.)

### -param ppv [out]

Type: <b>void**</b>

Receives a new <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a> object. (See usage remarks.)

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<h3><a id="Usage"></a><a id="usage"></a><a id="USAGE"></a>Usage</h3>
The <b>IID_PPV_ARGS</b> macro is generally used to generate the <i>riid</i> and <i>ppv</i> parameters for this function. For example:
            
                


```
#include "shobjidl.h"
#include "objbase.h" // Defines the IID_PPV_ARGS macro.        

...

IShellLibrary *pIShellLib;
SHCreateLibrary(IID_PPV_ARGS(&pIShellLib));

```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary">IShellLibrary</a>