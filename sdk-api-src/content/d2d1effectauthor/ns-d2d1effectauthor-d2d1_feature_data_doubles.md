---
UID: NS:d2d1effectauthor.D2D1_FEATURE_DATA_DOUBLES
title: D2D1_FEATURE_DATA_DOUBLES
author: windows-sdk-content
description: Describes the support for doubles in shaders.
old-location: direct2d\d2d1_feature_data_doubles.htm
tech.root: direct2d
ms.assetid: 29EDAD15-FFFF-4F0D-BB0D-B4BF37AC609F
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: D2D1_FEATURE_DATA_DOUBLES, D2D1_FEATURE_DATA_DOUBLES structure [Direct2D], d2d1effectauthor/D2D1_FEATURE_DATA_DOUBLES, direct2d.d2d1_feature_data_doubles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_FEATURE_DATA_DOUBLES
product: Windows
targetos: Windows
req.typenames: D2D1_FEATURE_DATA_DOUBLES
req.redist: 
---

# D2D1_FEATURE_DATA_DOUBLES structure


## -description


Describes the support for doubles in shaders.


## -struct-fields




### -field doublePrecisionFloatShaderOps

TRUE is doubles are supported within the shaders.


## -remarks



Fill this structure by passing a D2D1_FEATURE_DOUBLES structure to <a href="https://msdn.microsoft.com/1A97B928-7715-4D4E-AD38-7D01EE243494">ID2D1EffectContext::CheckFeatureSupport</a>.



