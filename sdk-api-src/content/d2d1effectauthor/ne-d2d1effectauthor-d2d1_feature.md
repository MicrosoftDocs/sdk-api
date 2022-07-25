---
UID: NE:d2d1effectauthor.D2D1_FEATURE
title: D2D1_FEATURE (d2d1effectauthor.h)
description: Defines capabilities of the underlying Direct3D device which may be queried using ID2D1EffectContext::CheckFeatureSupport.
helpviewer_keywords: ["D2D1_FEATURE","D2D1_FEATURE enumeration [Direct2D]","D2D1_FEATURE_D3D10_X_HARDWARE_OPTIONS","D2D1_FEATURE_DOUBLES","d2d1effectauthor/D2D1_FEATURE","d2d1effectauthor/D2D1_FEATURE_D3D10_X_HARDWARE_OPTIONS","d2d1effectauthor/D2D1_FEATURE_DOUBLES","direct2d.d2d1_feature"]
old-location: direct2d\d2d1_feature.htm
tech.root: Direct2D
ms.assetid: 1C64F1BE-DB38-440A-A1BA-65A40E5A9997
ms.date: 12/05/2018
ms.keywords: D2D1_FEATURE, D2D1_FEATURE enumeration [Direct2D], D2D1_FEATURE_D3D10_X_HARDWARE_OPTIONS, D2D1_FEATURE_DOUBLES, d2d1effectauthor/D2D1_FEATURE, d2d1effectauthor/D2D1_FEATURE_D3D10_X_HARDWARE_OPTIONS, d2d1effectauthor/D2D1_FEATURE_DOUBLES, direct2d.d2d1_feature
req.header: d2d1effectauthor.h
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
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_FEATURE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FEATURE
 - d2d1effectauthor/D2D1_FEATURE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_FEATURE
---

# D2D1_FEATURE enumeration


## -description

Defines capabilities of the underlying Direct3D device which may be queried using <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport">ID2D1EffectContext::CheckFeatureSupport</a>.

## -enum-fields

### -field D2D1_FEATURE_DOUBLES:0

A D2D1_FEATURE_DATA_DOUBLES structure should be filled.

### -field D2D1_FEATURE_D3D10_X_HARDWARE_OPTIONS:1

A D2D1_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS structure should be filled.

### -field D2D1_FEATURE_FORCE_DWORD:0xffffffff
