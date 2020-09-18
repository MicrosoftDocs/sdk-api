---
UID: NF:xamlom.IVisualTreeService.CreateInstance
title: IVisualTreeService::CreateInstance (xamlom.h)
description: Creates an instance of any XAML runtime, enum, or primitive type.
helpviewer_keywords: ["CreateInstance","CreateInstance method","CreateInstance method","IVisualTreeService interface","IVisualTreeService interface","CreateInstance method","IVisualTreeService.CreateInstance","IVisualTreeService::CreateInstance","xaml_diagnostics.ivisualtreeservice_createinstance","xamlom/IVisualTreeService::CreateInstance"]
old-location: xaml_diagnostics\ivisualtreeservice_createinstance.htm
tech.root: xaml_diagnostics
ms.assetid: 214BE795-5883-4761-9040-2C7A679F5258
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method, CreateInstance method,IVisualTreeService interface, IVisualTreeService interface,CreateInstance method, IVisualTreeService.CreateInstance, IVisualTreeService::CreateInstance, xaml_diagnostics.ivisualtreeservice_createinstance, xamlom/IVisualTreeService::CreateInstance
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
 - IVisualTreeService::CreateInstance
 - xamlom/IVisualTreeService::CreateInstance
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
 - IVisualTreeService.CreateInstance
---

# IVisualTreeService::CreateInstance


## -description

Creates an instance of any XAML runtime, enum, or primitive type.

## -parameters

### -param typeName [in]

The type name. (Should be from <a href="/previous-versions/windows/desktop/api/xamlom/ns-xamlom-propertychainvalue">PropertyChainValue.Type</a>.)

### -param value [in]

The value to set on a primitive or enum type. <b>null</b> if creating a XAML runtime type.

### -param pInstanceHandle [out, retval]

An instance handle to newly created instance.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 For primitives and enums, <i>value</i> should be 
    set to desired value. For XAML runtime types, <i>value</i> should be <b>null</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>