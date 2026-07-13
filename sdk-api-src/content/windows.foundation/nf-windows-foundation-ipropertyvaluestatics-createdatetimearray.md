---
UID: NF:windows.foundation.IPropertyValueStatics.CreateDateTimeArray
title: IPropertyValueStatics::CreateDateTimeArray (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of DateTime values.
helpviewer_keywords: ["CreateDateTimeArray","CreateDateTimeArray method [Windows Runtime]","CreateDateTimeArray method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateDateTimeArray method","IPropertyValueStatics.CreateDateTimeArray","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateDateTimeArray","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateDateTimeArray","winrt.ipropertyvaluefactory_createdatetimearray","winrt.ipropertyvaluestatics_createdatetimearray"]
old-location: winrt\ipropertyvaluestatics_createdatetimearray.htm
tech.root: WinRT
ms.assetid: 0c0beb76-0089-46b9-bcc5-ed07320859a3
ms.date: 12/05/2018
ms.keywords: CreateDateTimeArray, CreateDateTimeArray method [Windows Runtime], CreateDateTimeArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateDateTimeArray method, IPropertyValueStatics.CreateDateTimeArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateDateTimeArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateDateTimeArray, winrt.ipropertyvaluefactory_createdatetimearray, winrt.ipropertyvaluestatics_createdatetimearray
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
 - IPropertyValueStatics::CreateDateTimeArray
 - windows.foundation/IPropertyValueStatics::CreateDateTimeArray
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
 - IPropertyValueStatics.CreateDateTimeArray
---

# IPropertyValueStatics::CreateDateTimeArray (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> values.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.

### -param value [in]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a>*</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-datetime">DateTime</a> values to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getdatetimearray">IPropertyValue::GetDateTimeArray</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
