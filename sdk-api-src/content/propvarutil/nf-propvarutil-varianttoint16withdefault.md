---
UID: NF:propvarutil.VariantToInt16WithDefault
title: VariantToInt16WithDefault function (propvarutil.h)
description: Extracts an Int16 property value of a variant structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["VariantToInt16WithDefault","VariantToInt16WithDefault function [Windows Properties]","_shell_VariantToInt16WithDefault","properties.VariantToInt16WithDefault","propvarutil/VariantToInt16WithDefault","shell.VariantToInt16WithDefault"]
old-location: properties\VariantToInt16WithDefault.htm
tech.root: properties
ms.assetid: 4d6d0b7d-ae20-456c-9ef4-97fa682ece8b
ms.date: 12/05/2018
ms.keywords: VariantToInt16WithDefault, VariantToInt16WithDefault function [Windows Properties], _shell_VariantToInt16WithDefault, properties.VariantToInt16WithDefault, propvarutil/VariantToInt16WithDefault, shell.VariantToInt16WithDefault
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
 - VariantToInt16WithDefault
 - propvarutil/VariantToInt16WithDefault
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
 - VariantToInt16WithDefault
---

# VariantToInt16WithDefault function


## -description

Extracts an <b>Int16</b> property value of a variant structure. If no value exists, then the specified default value is returned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param iDefault [in]

Type: <b>SHORT</b>

Specifies default property value, for use where no value currently exists.

## -returns

Type: <b>SHORT</b>

Returns the extracted <b>Int16</b> value, or default.

