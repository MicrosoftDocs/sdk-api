---
UID: NF:d2d1_1helper.CreationProperties
title: CreationProperties function (d2d1_1helper.h)
description: Returns a D2D1_CREATION_PROPERTIES that describes root-level creation details.
helpviewer_keywords: ["CreationProperties","CreationProperties function [Direct2D]","d2d1_1helper/CreationProperties","direct2d.creationproperties"]
old-location: direct2d\creationproperties.htm
tech.root: Direct2D
ms.assetid: 81D88AFE-77B9-4871-9832-7323CAAB39CF
ms.date: 12/05/2018
ms.keywords: CreationProperties, CreationProperties function [Direct2D], d2d1_1helper/CreationProperties, direct2d.creationproperties
req.header: d2d1_1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreationProperties
 - d2d1_1helper/CreationProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - CreationProperties
---

# CreationProperties function


## -description

Returns a  <a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_creation_properties">D2D1_CREATION_PROPERTIES</a> that describes root-level creation details.

## -parameters

### -param threadingMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_threading_mode">D2D1_THREADING_MODE</a></b>

The threading mode with which the corresponding root objects are created.

### -param debugLevel

Type: <b><a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_debug_level">D2D1_DEBUG_LEVEL</a></b>

The debug level that the root objects should be created with.

### -param options

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options">D2D1_DEVICE_CONTEXT_OPTIONS</a></b>

The device context options that the root objects should be created with.

## -returns

Type: <b><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_creation_properties">D2D1_CREATION_PROPERTIES</a></b>

The filled creation properties structure.