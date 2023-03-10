---
UID: NF:d2d1_1.ID2D1Properties.GetSubProperties(UINT32,ID2D1Properties)
title: ID2D1Properties::GetSubProperties (d2d1_1.h)
description: Gets the sub-properties of the provided property by index.
helpviewer_keywords: ["GetSubProperties","GetSubProperties method [Direct2D]","GetSubProperties method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetSubProperties method","ID2D1Properties.GetSubProperties","ID2D1Properties::GetSubProperties","ID2D1Properties::GetSubProperties(UINT32","ID2D1Properties)","ID2D1Properties::GetSubProperties(UINT32","ID2D1Properties**)","d2d1_1/ID2D1Properties::GetSubProperties","direct2d.id2d1properties_getsubproperties"]
old-location: direct2d\id2d1properties_getsubproperties.htm
tech.root: Direct2D
ms.assetid: 6ba7ba8e-63fd-44a1-9a03-565b2e2a128c
ms.date: 12/05/2018
ms.keywords: GetSubProperties, GetSubProperties method [Direct2D], GetSubProperties method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetSubProperties method, ID2D1Properties.GetSubProperties, ID2D1Properties::GetSubProperties, ID2D1Properties::GetSubProperties(UINT32,ID2D1Properties), ID2D1Properties::GetSubProperties(UINT32,ID2D1Properties**), d2d1_1/ID2D1Properties::GetSubProperties, direct2d.id2d1properties_getsubproperties
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
 - ID2D1Properties::GetSubProperties
 - d2d1_1/ID2D1Properties::GetSubProperties
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
 - ID2D1Properties.GetSubProperties
---

# ID2D1Properties::GetSubProperties


## -description

Gets the sub-properties of the provided property by index.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the  sub-properties to be retrieved.

### -param subProperties [out]

Type: <b><a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>**</b>

When this method returns, contains the address of a pointer to the sub-properties.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>D2DERR_NO_SUBPROPERTIES</td>
<td>The specified property does not exist.</td>
</tr>
</table>

## -remarks

If there are no sub-properties, <i>subProperties</i> will be <b>NULL</b>, and <b>D2DERR_NO_SUBPROPERTIES</b> will be returned.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>