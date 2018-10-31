---
UID: NF:windows.foundation.IPropertyValue.GetInt64
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the signed 64-bit integer value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getint64.htm
tech.root: WinRT
ms.assetid: FA3EB6F4-8D5A-4DBE-9A49-D21BC5A57EF3
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetInt64, GetInt64 method [Windows Runtime], GetInt64 method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetInt64 method, IPropertyValue.GetInt64, IPropertyValue.IPropertyValue, IPropertyValue::GetInt64, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetInt64, winrt.ipropertyvalue_getint64
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
 - IPropertyValue.GetInt64
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the signed 64-bit integer value that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param value [out, retval]

Type: <b>INT64*</b>

The signed 64-bit integer value.


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



<a href="https://msdn.microsoft.com/70533BB7-E844-459C-ACA3-D76142B379F4">IPropertyValueStatics::CreateInt64</a>
 

 

