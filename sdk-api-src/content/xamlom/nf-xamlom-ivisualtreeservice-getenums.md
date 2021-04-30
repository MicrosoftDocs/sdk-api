---
UID: NF:xamlom.IVisualTreeService.GetEnums
title: IVisualTreeService::GetEnums (xamlom.h)
description: Gets an array of all the enums defined in the XAML runtime and the total count.
helpviewer_keywords: ["GetEnums","GetEnums method","GetEnums method","IVisualTreeService interface","IVisualTreeService interface","GetEnums method","IVisualTreeService.GetEnums","IVisualTreeService::GetEnums","xaml_diagnostics.ivisualtreeservice_getenums","xamlom/IVisualTreeService::GetEnums"]
old-location: xaml_diagnostics\ivisualtreeservice_getenums.htm
tech.root: xaml_diagnostics
ms.assetid: 95D6F754-C1D0-4B8E-8E31-999CAE0EDF02
ms.date: 12/05/2018
ms.keywords: GetEnums, GetEnums method, GetEnums method,IVisualTreeService interface, IVisualTreeService interface,GetEnums method, IVisualTreeService.GetEnums, IVisualTreeService::GetEnums, xaml_diagnostics.ivisualtreeservice_getenums, xamlom/IVisualTreeService::GetEnums
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
 - IVisualTreeService::GetEnums
 - xamlom/IVisualTreeService::GetEnums
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
 - IVisualTreeService.GetEnums
---

# IVisualTreeService::GetEnums


## -description

Gets an array of all the enums defined in the XAML runtime and the total
    count.

## -parameters

### -param pCount [out]

The count of enums in the array.

### -param ppEnums [out]

An array of enums defined in the XAML runtime.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. This method should not fail in normal conditions.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>