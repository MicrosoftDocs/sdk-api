---
UID: NF:directxcollision.BoundingFrustum.Transform
title: BoundingFrustum::Transform
description: Transforms the BoundingFrustum by the specified transformation matrix.helpviewer_keywords: ["BoundingFrustum::Transform"]
ms.date: 04/22/19
ms.keywords: BoundingFrustum::Transform
f1_keywords:
- directxcollision/BoundingFrustum::Transform
dev_langs:
- c++
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: directxcollision.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- 
api_location:
- directxcollision.h
api_name:
- BoundingFrustum::Transform
---

# BoundingFrustum.Transform(BoundingFrustum&, XMMATRIX) method

## -description

Transforms the **BoundingFrustum** by the specified transformation matrix.

## -parameters

### -param Out

The transformed **BoundingFrustum**.

### -param M

The transformation matrix.

**Note**  The transformation matrix cannot contain a scale transform.

## -returns

This method does not return a value.

## -remarks

### Platform Requirements

Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.
Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.

## -see-also

[BoundingFrustum](/windows/win32/api/directxcollision/ns-directxcollision-boundingfrustum)
