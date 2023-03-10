---
UID: NF:propvarutil.VariantToStrRet
title: VariantToStrRet function (propvarutil.h)
description: If the source variant is a VT_BSTR, extracts string and places it into a STRRET structure.
helpviewer_keywords: ["VariantToStrRet","VariantToStrRet function [Windows Properties]","_shell_VariantToStrRet","properties.VariantToStrRet","propvarutil/VariantToStrRet","shell.VariantToStrRet"]
old-location: properties\VariantToStrRet.htm
tech.root: properties
ms.assetid: dfc1f52e-58c6-48fd-8da9-1d4d5115912c
ms.date: 12/05/2018
ms.keywords: VariantToStrRet, VariantToStrRet function [Windows Properties], _shell_VariantToStrRet, properties.VariantToStrRet, propvarutil/VariantToStrRet, shell.VariantToStrRet
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantToStrRet
 - propvarutil/VariantToStrRet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToStrRet
---

# VariantToStrRet function


## -description

If the source variant is a VT_BSTR, extracts string and places it into a <a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a> structure.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pstrret [out]

Type: <b><a href="/windows/desktop/api/shtypes/ns-shtypes-strret">STRRET</a>*</b>

Pointer to the extracted string if one exists.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.