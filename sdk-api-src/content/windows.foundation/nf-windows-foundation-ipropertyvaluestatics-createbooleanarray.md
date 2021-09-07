---
UID: NF:windows.foundation.IPropertyValueStatics.CreateBooleanArray
title: IPropertyValueStatics::CreateBooleanArray (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of 8-bit Boolean values.
helpviewer_keywords: ["CreateBooleanArray","CreateBooleanArray method [Windows Runtime]","CreateBooleanArray method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateBooleanArray method","IPropertyValueStatics.CreateBooleanArray","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateBooleanArray","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateBooleanArray","winrt.ipropertyvaluefactory_createbooleanarray","winrt.ipropertyvaluestatics_createbooleanarray"]
old-location: winrt\ipropertyvaluestatics_createbooleanarray.htm
tech.root: WinRT
ms.assetid: 54289d10-8393-4c49-9087-873519b32aa8
ms.date: 12/05/2018
ms.keywords: CreateBooleanArray, CreateBooleanArray method [Windows Runtime], CreateBooleanArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateBooleanArray method, IPropertyValueStatics.CreateBooleanArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateBooleanArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateBooleanArray, winrt.ipropertyvaluefactory_createbooleanarray, winrt.ipropertyvaluestatics_createbooleanarray
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
 - IPropertyValueStatics::CreateBooleanArray
 - windows.foundation/IPropertyValueStatics::CreateBooleanArray
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
 - IPropertyValueStatics.CreateBooleanArray
---

# IPropertyValueStatics::CreateBooleanArray (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of 8-bit Boolean values.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.

### -param value [in]

Type: <b>boolean*</b>

The array of 8-bit Boolean values to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getbooleanarray">IPropertyValue::GetBooleanArray</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
