---
UID: NF:windows.foundation.IPropertyValueStatics.CreateUInt8Array
title: IPropertyValueStatics::CreateUInt8Array (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of unsigned 8-bit integer values.
helpviewer_keywords: ["CreateUInt8Array","CreateUInt8Array method [Windows Runtime]","CreateUInt8Array method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateUInt8Array method","IPropertyValueStatics.CreateUInt8Array","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateUInt8Array","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateUInt8Array","winrt.ipropertyvaluefactory_createuint8array","winrt.ipropertyvaluestatics_createuint8array"]
old-location: winrt\ipropertyvaluestatics_createuint8array.htm
tech.root: WinRT
ms.assetid: fc666379-4992-47da-b97b-b296219e26c1
ms.date: 12/05/2018
ms.keywords: CreateUInt8Array, CreateUInt8Array method [Windows Runtime], CreateUInt8Array method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateUInt8Array method, IPropertyValueStatics.CreateUInt8Array, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateUInt8Array, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateUInt8Array, winrt.ipropertyvaluefactory_createuint8array, winrt.ipropertyvaluestatics_createuint8array
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
 - IPropertyValueStatics::CreateUInt8Array
 - windows.foundation/IPropertyValueStatics::CreateUInt8Array
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
 - IPropertyValueStatics.CreateUInt8Array
---

# IPropertyValueStatics::CreateUInt8Array (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of unsigned 8-bit integer values.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.

### -param value [in]

Type: <b>BYTE*</b>

The array of unsigned 8-bit integer values to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint8array">IPropertyValue::GetUInt8Array</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
