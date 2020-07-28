---
UID: NF:d2d1_1.ID2D1Properties.GetType(UINT32)
title: ID2D1Properties::GetType (d2d1_1.h)
description: Gets the D2D1_PROPERTY_TYPE of the selected property.
helpviewer_keywords: ["GetType","GetType method [Direct2D]","GetType method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetType method","ID2D1Properties.GetType","ID2D1Properties::GetType","ID2D1Properties::GetType(UINT32)","d2d1_1/ID2D1Properties::GetType","direct2d.id2d1properties_gettype"]
old-location: direct2d\id2d1properties_gettype.htm
tech.root: Direct2D
ms.assetid: 42e80588-9e80-4f30-9a3c-77b64f88ff7a
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Direct2D], GetType method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetType method, ID2D1Properties.GetType, ID2D1Properties::GetType, ID2D1Properties::GetType(UINT32), d2d1_1/ID2D1Properties::GetType, direct2d.id2d1properties_gettype
f1_keywords:
- d2d1_1/ID2D1Properties.GetType
dev_langs:
- c++
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Properties.GetType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Properties::GetType


## -description


Gets the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a> of the selected property.




## -parameters




### -param index

Type: <b>UINT32</b>

The index of the property for which the type will be retrieved.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a></b>

This method returns a <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a>-typed value for the type of the selected property.




## -remarks



If the property does not exist, the method returns <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE_UNKNOWN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property_type">D2D1_PROPERTY_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>
 

 

