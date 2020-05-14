---
UID: NF:propvarutil.VariantToUInt16
title: VariantToUInt16 function (propvarutil.h)
description: Extracts an unsigned Int16 property value of a variant structure. If no value can be extracted, then a default value is assigned by this function.helpviewer_keywords: ["VariantToUInt16","VariantToUInt16 function [Windows Properties]","_shell_VariantToUInt16","properties.VariantToUInt16","propvarutil/VariantToUInt16","shell.VariantToUInt16"]
old-location: properties\VariantToUInt16.htm
tech.root: properties
ms.assetid: aa88be72-9ea5-4668-a0c5-1ca5320bda00
ms.date: 12/05/2018
ms.keywords: VariantToUInt16, VariantToUInt16 function [Windows Properties], _shell_VariantToUInt16, properties.VariantToUInt16, propvarutil/VariantToUInt16, shell.VariantToUInt16
f1_keywords:
- propvarutil/VariantToUInt16
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
- VariantToUInt16
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# VariantToUInt16 function


## -description


Extracts an unsigned <b>Int16</b> property value of a variant structure. If no value can be extracted, then a default value is assigned by this function.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param puiRet [out]

Type: <b>USHORT*</b>

Pointer to the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



