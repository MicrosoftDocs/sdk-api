---
UID: NF:windows.foundation.IPropertyValueStatics.CreatePointArray
title: IPropertyValueStatics::CreatePointArray (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of Point values.
helpviewer_keywords: ["CreatePointArray","CreatePointArray method [Windows Runtime]","CreatePointArray method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreatePointArray method","IPropertyValueStatics.CreatePointArray","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreatePointArray","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreatePointArray","winrt.ipropertyvaluefactory_createpointarray","winrt.ipropertyvaluestatics_createpointarray"]
old-location: winrt\ipropertyvaluestatics_createpointarray.htm
tech.root: WinRT
ms.assetid: cdfc2a91-0f1b-41d9-99e3-e3589bdae6ca
ms.date: 12/05/2018
ms.keywords: CreatePointArray, CreatePointArray method [Windows Runtime], CreatePointArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreatePointArray method, IPropertyValueStatics.CreatePointArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreatePointArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreatePointArray, winrt.ipropertyvaluefactory_createpointarray, winrt.ipropertyvaluestatics_createpointarray
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
 - IPropertyValueStatics::CreatePointArray
 - windows.foundation/IPropertyValueStatics::CreatePointArray
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
 - IPropertyValueStatics.CreatePointArray
---

# IPropertyValueStatics::CreatePointArray (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> values.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.

### -param value [in]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a>*</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-point">Point</a> values to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getpointarray">IPropertyValue::GetPointArray</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
