---
UID: NF:xamlom.IVisualTreeService.GetPropertyValuesChain
title: IVisualTreeService::GetPropertyValuesChain (xamlom.h)
description: Gets an array of all the properties set on the element passed in, and an array of all the styles involved in setting the effective values of the properties.
helpviewer_keywords: ["GetPropertyValuesChain","GetPropertyValuesChain method","GetPropertyValuesChain method","IVisualTreeService interface","IVisualTreeService interface","GetPropertyValuesChain method","IVisualTreeService.GetPropertyValuesChain","IVisualTreeService::GetPropertyValuesChain","xaml_diagnostics.ivisualtreeservice_getpropertyvalueschain","xamlom/IVisualTreeService::GetPropertyValuesChain"]
old-location: xaml_diagnostics\ivisualtreeservice_getpropertyvalueschain.htm
tech.root: xaml_diagnostics
ms.assetid: 3D997B09-7B20-47BC-B19C-98945CA41D17
ms.date: 12/05/2018
ms.keywords: GetPropertyValuesChain, GetPropertyValuesChain method, GetPropertyValuesChain method,IVisualTreeService interface, IVisualTreeService interface,GetPropertyValuesChain method, IVisualTreeService.GetPropertyValuesChain, IVisualTreeService::GetPropertyValuesChain, xaml_diagnostics.ivisualtreeservice_getpropertyvalueschain, xamlom/IVisualTreeService::GetPropertyValuesChain
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
 - IVisualTreeService::GetPropertyValuesChain
 - xamlom/IVisualTreeService::GetPropertyValuesChain
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
 - IVisualTreeService.GetPropertyValuesChain
---

# IVisualTreeService::GetPropertyValuesChain


## -description

Gets an array of all the
    properties set on the element passed in, and an array of all the styles involved in setting the effective values of the properties.

## -parameters

### -param instanceHandle [in]

A handle to the element to query properties on.

### -param pSourceCount [out]

The count of the property sources array.

### -param ppPropertySources [out]

An array of property sources.

### -param pPropertyCount [out]

The count of the property values array.

### -param ppPropertyValues [out]

An array of property values.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. This 
    method should not fail in normal conditions.

## -remarks

<b>GetPropertyValuesChain</b> returns an array of <a href="/previous-versions/windows/desktop/api/xamlom/ns-xamlom-propertychainvalue">PropertyChainValue</a> structs that represents all the
    properties set on the element passed in. It also returns an array of <a href="/previous-versions/windows/desktop/api/xamlom/ns-xamlom-propertychainsource">PropertyChainSource</a> structs that represents all the styles involved in setting the effective value of each property.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>