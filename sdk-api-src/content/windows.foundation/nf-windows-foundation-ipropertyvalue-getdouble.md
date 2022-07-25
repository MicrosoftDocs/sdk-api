---
UID: NF:windows.foundation.IPropertyValue.GetDouble
title: IPropertyValue::GetDouble (windows.foundation.h)
description: Gets the 64-bit floating point value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetDouble","GetDouble method [Windows Runtime]","GetDouble method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetDouble method","IPropertyValue.GetDouble","IPropertyValue.IPropertyValue","IPropertyValue::GetDouble","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetDouble","winrt.ipropertyvalue_getdouble"]
old-location: winrt\ipropertyvalue_getdouble.htm
tech.root: WinRT
ms.assetid: 93EC7793-DAEF-4E1D-A9B8-2D79A3CBBBDC
ms.date: 12/05/2018
ms.keywords: GetDouble, GetDouble method [Windows Runtime], GetDouble method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetDouble method, IPropertyValue.GetDouble, IPropertyValue.IPropertyValue, IPropertyValue::GetDouble, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetDouble, winrt.ipropertyvalue_getdouble
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
 - IPropertyValue::GetDouble
 - windows.foundation/IPropertyValue::GetDouble
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
 - IPropertyValue.GetDouble
---

# IPropertyValue::GetDouble (windows.foundation.h)


## -description

Gets the 64-bit floating point value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b>DOUBLE*</b>

The 64-bit floating point value.

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
The  property value was returned successfully.

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
<dt><b>E_INCORRECT_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of <i>value</i> does not match the <a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-get_type">Type</a> property.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createdouble">IPropertyValueStatics::CreateDouble</a>
