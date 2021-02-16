---
UID: NF:xamlom.IVisualTreeService.ClearProperty
title: IVisualTreeService::ClearProperty (xamlom.h)
description: Clears the specified property on a XAML element.
helpviewer_keywords: ["ClearProperty","ClearProperty method","ClearProperty method","IVisualTreeService interface","IVisualTreeService interface","ClearProperty method","IVisualTreeService.ClearProperty","IVisualTreeService::ClearProperty","xaml_diagnostics.ivisualtreeservice_clearproperty","xamlom/IVisualTreeService::ClearProperty"]
old-location: xaml_diagnostics\ivisualtreeservice_clearproperty.htm
tech.root: xaml_diagnostics
ms.assetid: BB875AD0-271D-4913-9811-5A5102B3E331
ms.date: 12/05/2018
ms.keywords: ClearProperty, ClearProperty method, ClearProperty method,IVisualTreeService interface, IVisualTreeService interface,ClearProperty method, IVisualTreeService.ClearProperty, IVisualTreeService::ClearProperty, xaml_diagnostics.ivisualtreeservice_clearproperty, xamlom/IVisualTreeService::ClearProperty
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
 - IVisualTreeService::ClearProperty
 - xamlom/IVisualTreeService::ClearProperty
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
 - IVisualTreeService.ClearProperty
---

# IVisualTreeService::ClearProperty


## -description

Clears the specified property on a XAML element.

## -parameters

### -param instanceHandle [in]

A handle to the element to set the property on.

### -param propertyIndex [in]

The index (in the XAML runtime cache) of the property to clear.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>