---
UID: NF:windows.foundation.IPropertyValueStatics.CreateEmpty
title: IPropertyValueStatics::CreateEmpty (windows.foundation.h)
description: Creates a new IPropertyValue object that represents an empty value.
helpviewer_keywords: ["CreateEmpty","CreateEmpty method [Windows Runtime]","CreateEmpty method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateEmpty method","IPropertyValueStatics.CreateEmpty","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateEmpty","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateEmpty","winrt.ipropertyvaluefactory_createempty","winrt.ipropertyvaluestatics_createempty"]
old-location: winrt\ipropertyvaluestatics_createempty.htm
tech.root: WinRT
ms.assetid: B1189E10-BB04-4648-87F9-447026E441D8
ms.date: 12/05/2018
ms.keywords: CreateEmpty, CreateEmpty method [Windows Runtime], CreateEmpty method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateEmpty method, IPropertyValueStatics.CreateEmpty, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateEmpty, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateEmpty, winrt.ipropertyvaluefactory_createempty, winrt.ipropertyvaluestatics_createempty
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
 - IPropertyValueStatics::CreateEmpty
 - windows.foundation/IPropertyValueStatics::CreateEmpty
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
 - IPropertyValueStatics.CreateEmpty
---

# IPropertyValueStatics::CreateEmpty (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that represents an empty value.

## -parameters

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that has its <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-get_type">Type</a> property set to <b>PropertyType_Empty</b>. No value is stored in the new object. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The  property value was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>value</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object could not be created.

</td>
</tr>
</table>

## -remarks

Use the <b>CreateEmpty</b>  method to represent an empty or unset property value in a property store.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
