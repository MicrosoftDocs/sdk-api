---
UID: NF:windows.foundation.IPropertyValueStatics.CreateRect
title: IPropertyValueStatics::CreateRect (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified Rect value.
helpviewer_keywords: ["CreateRect","CreateRect method [Windows Runtime]","CreateRect method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateRect method","IPropertyValueStatics.CreateRect","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateRect","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateRect","winrt.ipropertyvaluefactory_createrect","winrt.ipropertyvaluestatics_createrect"]
old-location: winrt\ipropertyvaluestatics_createrect.htm
tech.root: WinRT
ms.assetid: 2938c3e0-6383-4136-99a6-c47a04c331f7
ms.date: 12/05/2018
ms.keywords: CreateRect, CreateRect method [Windows Runtime], CreateRect method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateRect method, IPropertyValueStatics.CreateRect, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateRect, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateRect, winrt.ipropertyvaluefactory_createrect, winrt.ipropertyvaluestatics_createrect
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
 - IPropertyValueStatics::CreateRect
 - windows.foundation/IPropertyValueStatics::CreateRect
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
 - IPropertyValueStatics.CreateRect
---

# IPropertyValueStatics::CreateRect (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified <a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a> value.

## -parameters

### -param value [in]

Type: <b><a href="/windows/desktop/api/windows.foundation/ns-windows-foundation-rect">Rect</a></b>

The value to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getrect">IPropertyValue::GetRect</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
