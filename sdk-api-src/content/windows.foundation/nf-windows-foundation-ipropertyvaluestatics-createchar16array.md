---
UID: NF:windows.foundation.IPropertyValueStatics.CreateChar16Array
title: IPropertyValueStatics::CreateChar16Array (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of Unicode characters.
helpviewer_keywords: ["CreateChar16Array","CreateChar16Array method [Windows Runtime]","CreateChar16Array method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateChar16Array method","IPropertyValueStatics.CreateChar16Array","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateChar16Array","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateChar16Array","winrt.ipropertyvaluefactory_createchar16array","winrt.ipropertyvaluestatics_createchar16array"]
old-location: winrt\ipropertyvaluestatics_createchar16array.htm
tech.root: WinRT
ms.assetid: 4d78015a-dfe1-49be-8523-a5b0f96f7c58
ms.date: 12/05/2018
ms.keywords: CreateChar16Array, CreateChar16Array method [Windows Runtime], CreateChar16Array method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateChar16Array method, IPropertyValueStatics.CreateChar16Array, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateChar16Array, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateChar16Array, winrt.ipropertyvaluefactory_createchar16array, winrt.ipropertyvaluestatics_createchar16array
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
 - IPropertyValueStatics::CreateChar16Array
 - windows.foundation/IPropertyValueStatics::CreateChar16Array
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
 - IPropertyValueStatics.CreateChar16Array
---

# IPropertyValueStatics::CreateChar16Array (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of Unicode characters.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of Unicode characters in the array.

### -param value [in]

Type: <b>WCHAR*</b>

The array of Unicode characters to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getchar16array">IPropertyValue::GetChar16Array</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
