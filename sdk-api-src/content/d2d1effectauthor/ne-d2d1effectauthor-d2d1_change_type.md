---
UID: NE:d2d1effectauthor.D2D1_CHANGE_TYPE
title: D2D1_CHANGE_TYPE
author: windows-sdk-content
description: Describes flags that influence how the renderer interacts with a custom vertex shader.
old-location: direct2d\d2d1_change_type.htm
tech.root: direct2d
ms.assetid: 22960a80-1986-4ca0-98df-87f05e880e98
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D2D1_CHANGE_TYPE, D2D1_CHANGE_TYPE enumeration [Direct2D], D2D1_CHANGE_TYPE_CONTEXT, D2D1_CHANGE_TYPE_GRAPH, D2D1_CHANGE_TYPE_NONE, D2D1_CHANGE_TYPE_PROPERTIES, d2d1effectauthor/D2D1_CHANGE_TYPE, d2d1effectauthor/D2D1_CHANGE_TYPE_CONTEXT, d2d1effectauthor/D2D1_CHANGE_TYPE_GRAPH, d2d1effectauthor/D2D1_CHANGE_TYPE_NONE, d2d1effectauthor/D2D1_CHANGE_TYPE_PROPERTIES, direct2d.d2d1_change_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - D2D1_CHANGE_TYPE
product: Windows
targetos: Windows
req.typenames: D2D1_CHANGE_TYPE
req.redist: 
---

# D2D1_CHANGE_TYPE enumeration


## -description


Describes flags that influence how the renderer interacts with a custom vertex shader.


## -enum-fields




### -field D2D1_CHANGE_TYPE_NONE

There were no changes.


### -field D2D1_CHANGE_TYPE_PROPERTIES

The properties of the effect changed.


### -field D2D1_CHANGE_TYPE_CONTEXT

The context state changed.


### -field D2D1_CHANGE_TYPE_GRAPH

The effect’s transform graph has changed.  This happens only when an effect supports a variable input count.


### -field D2D1_CHANGE_TYPE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/0EBA4FDB-A9EA-4FCF-BF40-3D73ED356CD4">ID2D1EffectImpl::PrepareForRender</a>
 

 

