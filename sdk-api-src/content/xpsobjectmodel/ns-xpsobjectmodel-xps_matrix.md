---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0023
title: XPS_MATRIX (xpsobjectmodel.h)
description: Describes the left two columns of a 3-by-3 matrix.
helpviewer_keywords: ["XPS_MATRIX","XPS_MATRIX structure [XPS Documents and Packaging]","xps.xps_matrix","xpsobjectmodel/XPS_MATRIX"]
old-location: xps\xps_matrix.htm
tech.root: xps
ms.assetid: 0df75410-0e34-4962-8499-879d5153d9af
ms.date: 12/05/2018
ms.keywords: XPS_MATRIX, XPS_MATRIX structure [XPS Documents and Packaging], xps.xps_matrix, xpsobjectmodel/XPS_MATRIX
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_MATRIX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0023
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0023
 - XPS_MATRIX
 - xpsobjectmodel/XPS_MATRIX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_MATRIX
---

# XPS_MATRIX structure


## -description

Describes the left two columns of a 3-by-3 matrix.

## -struct-fields

### -field m11

The value in the left column of the first row of the matrix.

### -field m12

The value in the center column of the first row of the matrix.

### -field m21

The value in the left column of the second row of the matrix.

### -field m22

The value in the center column of the second row of the matrix.

### -field m31

The value in the left column of the third row of the matrix. This value is also the x-offset.

### -field m32

The value in the center column of the third row of the matrix. This value is also the y-offset.

## -remarks

The values in the third column of the matrix are assumed to be 0, 0, 1.

The following table shows the entire matrix.

<table>
<tr>
<td>m11</td>
<td>m12</td>
<td> 0 </td>
</tr>
<tr>
<td>m21</td>
<td>m22</td>
<td> 0 </td>
</tr>
<tr>
<td>m31</td>
<td>m32</td>
<td> 1 </td>
</tr>
</table>

## -see-also

<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>

