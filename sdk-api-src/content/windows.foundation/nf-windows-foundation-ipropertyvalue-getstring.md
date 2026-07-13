---
UID: NF:windows.foundation.IPropertyValue.GetString
title: IPropertyValue::GetString (windows.foundation.h)
description: Gets the string value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetString","GetString method [Windows Runtime]","GetString method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetString method","IPropertyValue.GetString","IPropertyValue.IPropertyValue","IPropertyValue::GetString","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetString","winrt.ipropertyvalue_getstring"]
old-location: winrt\ipropertyvalue_getstring.htm
tech.root: WinRT
ms.assetid: 56376A64-78F7-4C28-B3A7-9CE6594342E4
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [Windows Runtime], GetString method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetString method, IPropertyValue.GetString, IPropertyValue.IPropertyValue, IPropertyValue::GetString, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetString, winrt.ipropertyvalue_getstring
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
 - IPropertyValue::GetString
 - windows.foundation/IPropertyValue::GetString
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
 - IPropertyValue.GetString
---

# IPropertyValue::GetString (windows.foundation.h)


## -description

Gets the string value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b><a href="/windows/desktop/WinRT/hstring">HSTRING</a>*</b>

The string value.

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



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createstring">IPropertyValueStatics::CreateString</a>
