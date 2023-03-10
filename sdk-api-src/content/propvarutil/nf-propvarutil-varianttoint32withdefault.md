---
UID: NF:propvarutil.VariantToInt32WithDefault
title: VariantToInt32WithDefault function (propvarutil.h)
description: Extracts an Int32 property value of a variant structure. If no value exists, then the specified default value is returned.
helpviewer_keywords: ["VariantToInt32WithDefault","VariantToInt32WithDefault function [Windows Properties]","_shell_VariantToInt32WithDefault","properties.VariantToInt32WithDefault","propvarutil/VariantToInt32WithDefault","shell.VariantToInt32WithDefault"]
old-location: properties\VariantToInt32WithDefault.htm
tech.root: properties
ms.assetid: fd2d5330-2b31-4dbb-b57b-4ca5579fa03f
ms.date: 12/05/2018
ms.keywords: VariantToInt32WithDefault, VariantToInt32WithDefault function [Windows Properties], _shell_VariantToInt32WithDefault, properties.VariantToInt32WithDefault, propvarutil/VariantToInt32WithDefault, shell.VariantToInt32WithDefault
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
 - VariantToInt32WithDefault
 - propvarutil/VariantToInt32WithDefault
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
 - VariantToInt32WithDefault
---

# VariantToInt32WithDefault function


## -description

Extracts an <b>Int32</b> property value of a variant structure. If no value exists, then the specified default value is returned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param lDefault [in]

Type: <b>LONG</b>

Specifies default property value, for use where no value currently exists.

## -returns

Type: <b>LONG</b>

Returns the extracted Int32 value, or default.

