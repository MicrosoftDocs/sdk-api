---
UID: NF:windows.foundation.IPropertyValue.GetUInt64
title: IPropertyValue::GetUInt64 (windows.foundation.h)
description: Gets the unsigned 64-bit integer value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetUInt64","GetUInt64 method [Windows Runtime]","GetUInt64 method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetUInt64 method","IPropertyValue.GetUInt64","IPropertyValue.IPropertyValue","IPropertyValue::GetUInt64","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetUInt64","winrt.ipropertyvalue_getuint64"]
old-location: winrt\ipropertyvalue_getuint64.htm
tech.root: WinRT
ms.assetid: 2FD209CA-9A8D-40F3-B82E-E80A7D212A5D
ms.date: 12/05/2018
ms.keywords: GetUInt64, GetUInt64 method [Windows Runtime], GetUInt64 method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetUInt64 method, IPropertyValue.GetUInt64, IPropertyValue.IPropertyValue, IPropertyValue::GetUInt64, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetUInt64, winrt.ipropertyvalue_getuint64
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
 - IPropertyValue::GetUInt64
 - windows.foundation/IPropertyValue::GetUInt64
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
 - IPropertyValue.GetUInt64
---

# IPropertyValue::GetUInt64 (windows.foundation.h)


## -description

Gets the unsigned 64-bit integer value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b>UINT64*</b>

The unsigned 64-bit integer value.

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



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createuint64">IPropertyValueStatics::CreateUInt64</a>
