---
UID: NF:propvarutil.VariantGetElementCount
title: VariantGetElementCount function (propvarutil.h)
description: Retrieves the element count of a variant structure.
helpviewer_keywords: ["VariantGetElementCount","VariantGetElementCount function [Windows Properties]","_shell_VariantGetElementCount","properties.VariantGetElementCount","propvarutil/VariantGetElementCount","shell.VariantGetElementCount"]
old-location: properties\VariantGetElementCount.htm
tech.root: properties
ms.assetid: 2bf96650-c0c4-4c99-9a04-d36d506b8f68
ms.date: 12/05/2018
ms.keywords: VariantGetElementCount, VariantGetElementCount function [Windows Properties], _shell_VariantGetElementCount, properties.VariantGetElementCount, propvarutil/VariantGetElementCount, shell.VariantGetElementCount
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
 - VariantGetElementCount
 - propvarutil/VariantGetElementCount
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
 - VariantGetElementCount
---

# VariantGetElementCount function


## -description

Retrieves the element count of a variant structure.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

## -returns

Type: <b>ULONG</b>

Returns the element count for values of type VT_ARRAY; otherwise, returns 1.

