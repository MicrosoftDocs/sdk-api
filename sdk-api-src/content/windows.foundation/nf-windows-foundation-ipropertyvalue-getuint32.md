---
UID: NF:windows.foundation.IPropertyValue.GetUInt32
title: IPropertyValue::GetUInt32 (windows.foundation.h)
description: Gets the unsigned 32-bit integer value that is stored in the current IPropertyValue object.
helpviewer_keywords: ["GetUInt32","GetUInt32 method [Windows Runtime]","GetUInt32 method [Windows Runtime]","IPropertyValue interface","IPropertyValue interface [Windows Runtime]","GetUInt32 method","IPropertyValue.GetUInt32","IPropertyValue.IPropertyValue","IPropertyValue::GetUInt32","IPropertyValue::IPropertyValue","windows/IPropertyValue::GetUInt32","winrt.ipropertyvalue_getuint32"]
old-location: winrt\ipropertyvalue_getuint32.htm
tech.root: WinRT
ms.assetid: 3675764D-7073-479B-8B9A-0AD037A963FB
ms.date: 12/05/2018
ms.keywords: GetUInt32, GetUInt32 method [Windows Runtime], GetUInt32 method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetUInt32 method, IPropertyValue.GetUInt32, IPropertyValue.IPropertyValue, IPropertyValue::GetUInt32, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetUInt32, winrt.ipropertyvalue_getuint32
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
 - IPropertyValue::GetUInt32
 - windows.foundation/IPropertyValue::GetUInt32
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
 - IPropertyValue.GetUInt32
---

# IPropertyValue::GetUInt32 (windows.foundation.h)


## -description

Gets the unsigned 32-bit integer value that is stored in the current <a href="/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.

## -parameters

### -param value [out, retval]

Type: <b>UINT32*</b>

The unsigned 32-bit integer value.

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



<a href="/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createuint32">IPropertyValueStatics::CreateUInt32</a>
