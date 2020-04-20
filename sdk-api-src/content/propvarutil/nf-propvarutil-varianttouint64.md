---
UID: NF:propvarutil.VariantToUInt64
title: VariantToUInt64 function (propvarutil.h)
description: Extracts unsigned Int64 property value of a variant structure. If no value can be extracted, then a default value is assigned.helpviewer_keywords: ["VariantToUInt64","VariantToUInt64 function [Windows Properties]","_shell_VariantToUInt64","properties.VariantToUInt64","propvarutil/VariantToUInt64","shell.VariantToUInt64"]
old-location: properties\VariantToUInt64.htm
tech.root: properties
ms.assetid: 1278f775-8439-4d05-acc9-b5207a3ccba7
ms.date: 12/05/2018
ms.keywords: VariantToUInt64, VariantToUInt64 function [Windows Properties], _shell_VariantToUInt64, properties.VariantToUInt64, propvarutil/VariantToUInt64, shell.VariantToUInt64
f1_keywords:
- propvarutil/VariantToUInt64
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Propsys.dll
api_name:
- VariantToUInt64
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# VariantToUInt64 function


## -description


Extracts unsigned <b>Int64</b> property value of a variant structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param pullRet [out]

Type: <b>ULONGLONG*</b>

Pointer to the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



