---
UID: NF:propvarutil.IsVariantString
title: IsVariantString function (propvarutil.h)
description: Specifies whether a variant is a string.
helpviewer_keywords: ["IsVariantString","IsVariantString function [Windows Properties]","_shell_IsVariantString","properties.IsVariantString","propvarutil/IsVariantString","shell.IsVariantString"]
old-location: properties\IsVariantString.htm
tech.root: properties
ms.assetid: 6056856c-9b7a-4c6a-9e9a-0baa5e1addcf
ms.date: 12/05/2018
ms.keywords: IsVariantString, IsVariantString function [Windows Properties], _shell_IsVariantString, properties.IsVariantString, propvarutil/IsVariantString, shell.IsVariantString
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IsVariantString
 - propvarutil/IsVariantString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - IsVariantString
---

# IsVariantString function


## -description

Specifies whether a variant is a string.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to the variant being queried.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if variant is a string.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.

