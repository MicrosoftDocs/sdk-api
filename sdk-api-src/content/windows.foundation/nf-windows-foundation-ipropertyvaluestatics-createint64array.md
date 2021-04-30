---
UID: NF:windows.foundation.IPropertyValueStatics.CreateInt64Array
title: IPropertyValueStatics::IPropertyValueStatics (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of signed 64-bit integer values.
helpviewer_keywords: ["CreateInt64Array","CreateInt64Array method [Windows Runtime]","CreateInt64Array method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateInt64Array method","IPropertyValueStatics.CreateInt64Array","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateInt64Array","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateInt64Array","winrt.ipropertyvaluefactory_createint64array","winrt.ipropertyvaluestatics_createint64array"]
old-location: winrt\ipropertyvaluestatics_createint64array.htm
tech.root: WinRT
ms.assetid: c226a049-e8e5-4283-a8c4-102beed08b23
ms.date: 12/05/2018
ms.keywords: CreateInt64Array, CreateInt64Array method [Windows Runtime], CreateInt64Array method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateInt64Array method, IPropertyValueStatics.CreateInt64Array, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateInt64Array, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateInt64Array, winrt.ipropertyvaluefactory_createint64array, winrt.ipropertyvaluestatics_createint64array
req.header: windows.foundation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Foundation.idl
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
 - IPropertyValueStatics::CreateInt64Array
 - windows.foundation/IPropertyValueStatics::CreateInt64Array
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValueStatics.CreateInt64Array
---

# IPropertyValueStatics::IPropertyValueStatics


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of signed 64-bit integer values.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.

### -param value [in]

Type: <b>INT64*</b>

The array of signed 64-bit integer values to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getint64array">IPropertyValue::GetInt64Array</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>