---
UID: NF:windows.foundation.IPropertyValueStatics.CreateUInt64
title: IPropertyValueStatics::CreateUInt64 (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified unsigned 64-bit integer value.
helpviewer_keywords: ["CreateUInt64","CreateUInt64 method [Windows Runtime]","CreateUInt64 method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateUInt64 method","IPropertyValueStatics.CreateUInt64","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateUInt64","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateUInt64","winrt.ipropertyvaluefactory_createuint64","winrt.ipropertyvaluestatics_createuint64"]
old-location: winrt\ipropertyvaluestatics_createuint64.htm
tech.root: WinRT
ms.assetid: 49158177-D74E-4310-984D-A1C511840EF9
ms.date: 12/05/2018
ms.keywords: CreateUInt64, CreateUInt64 method [Windows Runtime], CreateUInt64 method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateUInt64 method, IPropertyValueStatics.CreateUInt64, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateUInt64, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateUInt64, winrt.ipropertyvaluefactory_createuint64, winrt.ipropertyvaluestatics_createuint64
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
 - IPropertyValueStatics::CreateUInt64
 - windows.foundation/IPropertyValueStatics::CreateUInt64
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
 - IPropertyValueStatics.CreateUInt64
---

# IPropertyValueStatics::CreateUInt64 (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified unsigned 64-bit integer value.

## -parameters

### -param value [in]

Type: <b>UINT64</b>

The unsigned 64-bit integer value to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method to get the <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> interface for the object.

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

Use the <b>CreateUInt64</b> method to  store a value in an <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object. You can add the  <b>IPropertyValue</b> object to a property store. Use the <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint64">GetUInt64</a> method to retrieve the value from the  <b>IPropertyValue</b> object.

## -see-also

<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-getuint64">IPropertyValue::GetUInt64</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
