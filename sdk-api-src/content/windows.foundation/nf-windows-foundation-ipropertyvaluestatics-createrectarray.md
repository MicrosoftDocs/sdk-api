---
UID: NF:windows.foundation.IPropertyValueStatics.CreateRectArray
title: IPropertyValueStatics::CreateRectArray (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified array of Rect values.
helpviewer_keywords: ["CreateRectArray","CreateRectArray method [Windows Runtime]","CreateRectArray method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateRectArray method","IPropertyValueStatics.CreateRectArray","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateRectArray","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateRectArray","winrt.ipropertyvaluefactory_createrectarray","winrt.ipropertyvaluestatics_createrectarray"]
old-location: winrt\ipropertyvaluestatics_createrectarray.htm
tech.root: WinRT
ms.assetid: 945f9c0a-22fe-42f6-b29b-3260607345f7
ms.date: 12/05/2018
ms.keywords: CreateRectArray, CreateRectArray method [Windows Runtime], CreateRectArray method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateRectArray method, IPropertyValueStatics.CreateRectArray, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateRectArray, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateRectArray, winrt.ipropertyvaluefactory_createrectarray, winrt.ipropertyvaluestatics_createrectarray
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
 - IPropertyValueStatics::CreateRectArray
 - windows.foundation/IPropertyValueStatics::CreateRectArray
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
 - IPropertyValueStatics.CreateRectArray
---

# IPropertyValueStatics::CreateRectArray (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> values.

## -parameters

### -param __valueSize [in]

Type: <b>UINT32</b>

The number of values in the array.

### -param value [in]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a>*</b>

The array of <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> values to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getrectarray">IPropertyValue::GetRectArray</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
