---
UID: NF:xamlom.IVisualTreeService.SetProperty
title: IVisualTreeService::SetProperty (xamlom.h)
description: Sets a property value on a XAML element.
helpviewer_keywords: ["IVisualTreeService interface","SetProperty method","IVisualTreeService.SetProperty","IVisualTreeService::SetProperty","SetProperty","SetProperty method","SetProperty method","IVisualTreeService interface","xaml_diagnostics.ivisualtreeservice_setproperty","xamlom/IVisualTreeService::SetProperty"]
old-location: xaml_diagnostics\ivisualtreeservice_setproperty.htm
tech.root: xaml_diagnostics
ms.assetid: A9C6C67F-7767-454C-BA05-86C6B1E5D712
ms.date: 12/05/2018
ms.keywords: IVisualTreeService interface,SetProperty method, IVisualTreeService.SetProperty, IVisualTreeService::SetProperty, SetProperty, SetProperty method, SetProperty method,IVisualTreeService interface, xaml_diagnostics.ivisualtreeservice_setproperty, xamlom/IVisualTreeService::SetProperty
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
 - IVisualTreeService::SetProperty
 - xamlom/IVisualTreeService::SetProperty
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
 - IVisualTreeService.SetProperty
---

# IVisualTreeService::SetProperty


## -description

Sets a property value on a XAML element.

## -parameters

### -param instanceHandle [in]

A handle to the element to set the property on.

### -param value [in]

A handle to the value to set on the element property.

### -param propertyIndex [in]

The index (in the XAML runtime cache) of the property to set.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller of <b>SetProperty</b> must know the index of the property to be set by first calling
    <a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-getpropertyvalueschain">GetPropertyValuesChain</a> and finding the property they want to set and retrieving its index.
    They must also have an <b>InstanceHandle</b> to a value, either by calling <a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-createinstance">CreateInstance</a>, or caching
    an earlier instance of some shared property, such as <b>SolidColorBrush</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>