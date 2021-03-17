---
UID: NS:d2d1_1.D2D1_CREATION_PROPERTIES
title: D2D1_CREATION_PROPERTIES (d2d1_1.h)
description: Specifies the options with which the Direct2D device, factory, and device context are created.
helpviewer_keywords: ["D2D1_CREATION_PROPERTIES","D2D1_CREATION_PROPERTIES structure [Direct2D]","PD2D1_CREATION_PROPERTIES","PD2D1_CREATION_PROPERTIES structure pointer [Direct2D]","d2d1_1/D2D1_CREATION_PROPERTIES","d2d1_1/PD2D1_CREATION_PROPERTIES","direct2d.d2d1_creation_properties"]
old-location: direct2d\d2d1_creation_properties.htm
tech.root: Direct2D
ms.assetid: 657439fe-dc17-42af-9e2c-2f3cb769a5a3
ms.date: 12/05/2018
ms.keywords: D2D1_CREATION_PROPERTIES, D2D1_CREATION_PROPERTIES structure [Direct2D], PD2D1_CREATION_PROPERTIES, PD2D1_CREATION_PROPERTIES structure pointer [Direct2D], d2d1_1/D2D1_CREATION_PROPERTIES, d2d1_1/PD2D1_CREATION_PROPERTIES, direct2d.d2d1_creation_properties
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_CREATION_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_CREATION_PROPERTIES
 - d2d1_1/D2D1_CREATION_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_CREATION_PROPERTIES
---

# D2D1_CREATION_PROPERTIES structure


## -description

Specifies the options with which the <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device, factory, and device context are created.

## -struct-fields

### -field threadingMode

The threading mode with which the corresponding root objects will be created.

### -field debugLevel

The debug level that the root objects should be created with.

### -field options

The device context options that the root objects should be created with.

## -remarks

The root objects referred to here are the <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> device, Direct2D factory and the Direct2D device context.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice">D2D1CreateDevice</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext">D2D1CreateDeviceContext</a>