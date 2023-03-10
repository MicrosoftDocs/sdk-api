---
UID: NF:propvarutil.VariantToStringWithDefault
title: VariantToStringWithDefault function (propvarutil.h)
description: Extracts the string property value of a variant structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["VariantToStringWithDefault","VariantToStringWithDefault function [Windows Properties]","_shell_VariantToStringWithDefault","properties.VariantToStringWithDefault","propvarutil/VariantToStringWithDefault","shell.VariantToStringWithDefault"]
old-location: properties\VariantToStringWithDefault.htm
tech.root: properties
ms.assetid: f8ca7844-057f-4e95-a4a9-f03f1d2ad492
ms.date: 12/05/2018
ms.keywords: VariantToStringWithDefault, VariantToStringWithDefault function [Windows Properties], _shell_VariantToStringWithDefault, properties.VariantToStringWithDefault, propvarutil/VariantToStringWithDefault, shell.VariantToStringWithDefault
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
 - VariantToStringWithDefault
 - propvarutil/VariantToStringWithDefault
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
 - VariantToStringWithDefault
---

# VariantToStringWithDefault function


## -description

Extracts the string property value of a variant structure. If no value exists, then the specified default value is returned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pszDefault [in]

Type: <b>LPCWSTR</b>

Pointer to the default Unicode string property value, for use where no value currently exists.

## -returns

Type: <b>PCWSTR</b>

Returns the extracted string value, or default.

