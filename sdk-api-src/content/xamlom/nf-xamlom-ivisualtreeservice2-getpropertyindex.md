---
UID: NF:xamlom.IVisualTreeService2.GetPropertyIndex
title: IVisualTreeService2::GetPropertyIndex (xamlom.h)
description: Gets the property index for the specified property name.
helpviewer_keywords: ["GetPropertyIndex","GetPropertyIndex method","GetPropertyIndex method","IVisualTreeService2 interface","IVisualTreeService2 interface","GetPropertyIndex method","IVisualTreeService2.GetPropertyIndex","IVisualTreeService2::GetPropertyIndex","xaml_diagnostics.ivisualtreeservice2_getpropertyindex","xamlom/IVisualTreeService2::GetPropertyIndex"]
old-location: xaml_diagnostics\ivisualtreeservice2_getpropertyindex.htm
tech.root: xaml_diagnostics
ms.assetid: E23FA0C6-7822-4CEA-AF0C-75B42941B143
ms.date: 12/05/2018
ms.keywords: GetPropertyIndex, GetPropertyIndex method, GetPropertyIndex method,IVisualTreeService2 interface, IVisualTreeService2 interface,GetPropertyIndex method, IVisualTreeService2.GetPropertyIndex, IVisualTreeService2::GetPropertyIndex, xaml_diagnostics.ivisualtreeservice2_getpropertyindex, xamlom/IVisualTreeService2::GetPropertyIndex
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVisualTreeService2::GetPropertyIndex
 - xamlom/IVisualTreeService2::GetPropertyIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IVisualTreeService2.GetPropertyIndex
---

# IVisualTreeService2::GetPropertyIndex


## -description

Gets the property index for the specified property name.

## -parameters

### -param object [in]

The dependency object to get the property index from.

### -param propertyName [in]

The name of the dependency property for which to get the index.

### -param pPropertyIndex [out]

The index of the specified property.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No property with <i>propertyName</i> was found, or the property cannot be applied to <i>object</i>.

</td>
</tr>
</table>

## -remarks

This index can be passed to the <a href="/previous-versions/windows/desktop/xaml_diagnostics/ivisualtreeservice2-getproperty">GetProperty</a> method in order to retrieve a specific property on an object.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice2">IVisualTreeService2</a>