---
UID: NF:d2d1_1.ID2D1Properties.GetPropertyNameLength(UINT32)
title: ID2D1Properties::GetPropertyNameLength (d2d1_1.h)
description: Gets the number of characters for the given property name.
helpviewer_keywords: ["GetPropertyNameLength","GetPropertyNameLength method [Direct2D]","GetPropertyNameLength method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetPropertyNameLength method","ID2D1Properties.GetPropertyNameLength","ID2D1Properties::GetPropertyNameLength","ID2D1Properties::GetPropertyNameLength(UINT32)","d2d1_1/ID2D1Properties::GetPropertyNameLength","direct2d.id2d1properties_getpropertynamelength"]
old-location: direct2d\id2d1properties_getpropertynamelength.htm
tech.root: Direct2D
ms.assetid: 9c4b86d1-db5b-41cd-9dd4-85a8bb03dd20
ms.date: 12/05/2018
ms.keywords: GetPropertyNameLength, GetPropertyNameLength method [Direct2D], GetPropertyNameLength method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetPropertyNameLength method, ID2D1Properties.GetPropertyNameLength, ID2D1Properties::GetPropertyNameLength, ID2D1Properties::GetPropertyNameLength(UINT32), d2d1_1/ID2D1Properties::GetPropertyNameLength, direct2d.id2d1properties_getpropertynamelength
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Properties::GetPropertyNameLength
 - d2d1_1/ID2D1Properties::GetPropertyNameLength
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
 - ID2D1Properties.GetPropertyNameLength
---

# ID2D1Properties::GetPropertyNameLength


## -description

Gets  the number of characters for the given property name.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the property name to retrieve.

## -returns

Type: <b>UINT32</b>

This method returns the size in characters of the name corresponding to the given property index, or zero if the property index does not exist.

## -remarks

The value returned by this method can be used to ensure that the buffer size for <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyname(uint32_pwstr_uint32)">GetPropertyName</a> is appropriate.

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_property">D2D1_PROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_subproperty">D2D1_SUBPROPERTY</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">ID2D1DeviceContext::CreateEffect</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>