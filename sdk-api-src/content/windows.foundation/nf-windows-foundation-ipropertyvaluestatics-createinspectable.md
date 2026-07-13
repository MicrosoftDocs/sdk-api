---
UID: NF:windows.foundation.IPropertyValueStatics.CreateInspectable
title: IPropertyValueStatics::CreateInspectable (windows.foundation.h)
description: Creates a new IPropertyValue object that contains the specified IInspectable object.
helpviewer_keywords: ["CreateInspectable","CreateInspectable method [Windows Runtime]","CreateInspectable method [Windows Runtime]","IPropertyValueStatics interface","IPropertyValueStatics interface [Windows Runtime]","CreateInspectable method","IPropertyValueStatics.CreateInspectable","IPropertyValueStatics.IPropertyValueStatics","IPropertyValueStatics::CreateInspectable","IPropertyValueStatics::IPropertyValueStatics","windows/IPropertyValueStatics::CreateInspectable","winrt.ipropertyvaluefactory_createinspectable","winrt.ipropertyvaluestatics_createinspectable"]
old-location: winrt\ipropertyvaluestatics_createinspectable.htm
tech.root: WinRT
ms.assetid: 6FCAD9E9-AB44-4D26-BD75-26B1C25FA524
ms.date: 12/05/2018
ms.keywords: CreateInspectable, CreateInspectable method [Windows Runtime], CreateInspectable method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateInspectable method, IPropertyValueStatics.CreateInspectable, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateInspectable, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateInspectable, winrt.ipropertyvaluefactory_createinspectable, winrt.ipropertyvaluestatics_createinspectable
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
 - IPropertyValueStatics::CreateInspectable
 - windows.foundation/IPropertyValueStatics::CreateInspectable
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
 - IPropertyValueStatics.CreateInspectable
---

# IPropertyValueStatics::CreateInspectable (windows.foundation.h)


## -description

Creates a new <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object that contains  the specified <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> object.

## -parameters

### -param value [in]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>*</b>

The object to store.

### -param propertyValue [out, retval]

Type: <b><a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>.

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

Use the <b>CreateInspectable</b> method to  store a value in an <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object. You can add the  <b>IPropertyValue</b> object to a property store. Use the <a href="/previous-versions/visualstudio">GetInspectable</a> method to retrieve the value from the  <b>IPropertyValue</b> object.

## -see-also

<a href="/previous-versions/visualstudio">IPropertyValue::GetInspectable</a>



<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics">IPropertyValueStatics</a>
