---
UID: NF:d2d1_1.ID2D1Properties.GetPropertyCount
title: ID2D1Properties::GetPropertyCount (d2d1_1.h)
description: Gets the number of top-level properties.
helpviewer_keywords: ["GetPropertyCount","GetPropertyCount method [Direct2D]","GetPropertyCount method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetPropertyCount method","ID2D1Properties.GetPropertyCount","ID2D1Properties::GetPropertyCount","d2d1_1/ID2D1Properties::GetPropertyCount","direct2d.id2d1properties_getpropertycount"]
old-location: direct2d\id2d1properties_getpropertycount.htm
tech.root: Direct2D
ms.assetid: abf54fef-8b46-41f9-a87e-c9c58e8ee49e
ms.date: 12/05/2018
ms.keywords: GetPropertyCount, GetPropertyCount method [Direct2D], GetPropertyCount method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetPropertyCount method, ID2D1Properties.GetPropertyCount, ID2D1Properties::GetPropertyCount, d2d1_1/ID2D1Properties::GetPropertyCount, direct2d.id2d1properties_getpropertycount
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
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Properties::GetPropertyCount
 - d2d1_1/ID2D1Properties::GetPropertyCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties.GetPropertyCount
---

# ID2D1Properties::GetPropertyCount


## -description

Gets the number of top-level properties.



## -returns

Type: <b>UINT32</b>

This method returns the number of custom (non-system) properties that can be accessed by the object.

## -remarks

This method returns the number of custom properties on the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a> interface. System properties and sub-properties are part of a closed set, and are enumerable by iterating over this closed set.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
