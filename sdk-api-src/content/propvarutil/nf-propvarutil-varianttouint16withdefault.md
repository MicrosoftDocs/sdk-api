---
UID: NF:propvarutil.VariantToUInt16WithDefault
title: VariantToUInt16WithDefault function (propvarutil.h)
description: Extracts an unsigned Int16 property value of a variant structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["VariantToUInt16WithDefault","VariantToUInt16WithDefault function [Windows Properties]","_shell_VariantToUInt16WithDefault","properties.VariantToUInt16WithDefault","propvarutil/VariantToUInt16WithDefault","shell.VariantToUInt16WithDefault"]
old-location: properties\VariantToUInt16WithDefault.htm
tech.root: properties
ms.assetid: 937d64c3-f5af-4230-b811-6d5883ecaf86
ms.date: 12/05/2018
ms.keywords: VariantToUInt16WithDefault, VariantToUInt16WithDefault function [Windows Properties], _shell_VariantToUInt16WithDefault, properties.VariantToUInt16WithDefault, propvarutil/VariantToUInt16WithDefault, shell.VariantToUInt16WithDefault
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
 - VariantToUInt16WithDefault
 - propvarutil/VariantToUInt16WithDefault
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
 - VariantToUInt16WithDefault
---

# VariantToUInt16WithDefault function


## -description

Extracts an unsigned <b>Int16</b> property value of a variant structure. If no value exists, then the specified default value is returned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param uiDefault [in]

Type: <b>USHORT</b>

Specifies default property value, for use where no value currently exists.

## -returns

Type: <b>USHORT</b>

Returns extracted unsigned <b>Int16</b> value, or default.

