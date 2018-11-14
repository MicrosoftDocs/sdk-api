---
UID: NF:windows.foundation.IPropertyValue.GetUInt64
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the unsigned 64-bit integer value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getuint64.htm
tech.root: WinRT
ms.assetid: 2FD209CA-9A8D-40F3-B82E-E80A7D212A5D
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetUInt64, GetUInt64 method [Windows Runtime], GetUInt64 method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetUInt64 method, IPropertyValue.GetUInt64, IPropertyValue.IPropertyValue, IPropertyValue::GetUInt64, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetUInt64, winrt.ipropertyvalue_getuint64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Foundation.h
api_name:
 - IPropertyValue.GetUInt64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.foundation.h
: 
- IPropertyValue.GetUInt64
: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the unsigned 64-bit integer value that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


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
The type of <i>value</i> does not match the <a href="https://msdn.microsoft.com/8C6C042A-53AA-439B-8D8D-F67DB45CC3C6">Type</a> property.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/49158177-D74E-4310-984D-A1C511840EF9">IPropertyValueStatics::CreateUInt64</a>
 

 

