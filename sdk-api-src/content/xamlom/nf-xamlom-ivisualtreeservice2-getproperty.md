---
UID: NF:xamlom.IVisualTreeService2.GetProperty
title: IVisualTreeService2::GetProperty (xamlom.h)
description: Gets the effective value of the specified dependency property.
helpviewer_keywords: ["GetProperty","GetProperty method","GetProperty method","IVisualTreeService2 interface","IVisualTreeService2 interface","GetProperty method","IVisualTreeService2.GetProperty","IVisualTreeService2::GetProperty","xaml_diagnostics.ivisualtreeservice2_getproperty","xamlom/IVisualTreeService2::GetProperty"]
old-location: xaml_diagnostics\ivisualtreeservice2_getproperty.htm
tech.root: xaml_diagnostics
ms.assetid: 6FC5A7CF-A5EF-48B1-8DCD-4885BAFA0055
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method, GetProperty method,IVisualTreeService2 interface, IVisualTreeService2 interface,GetProperty method, IVisualTreeService2.GetProperty, IVisualTreeService2::GetProperty, xaml_diagnostics.ivisualtreeservice2_getproperty, xamlom/IVisualTreeService2::GetProperty
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
 - IVisualTreeService2::GetProperty
 - xamlom/IVisualTreeService2::GetProperty
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
 - IVisualTreeService2.GetProperty
---

# IVisualTreeService2::GetProperty


## -description

Gets the effective value of the specified dependency property.

## -parameters

### -param object [in]

The dependency object to get the property value from.

### -param propertyIndex [in]

The index of the  property to get the value from.

### -param pValue [out]

The effective value of the property.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice2">IVisualTreeService2</a>