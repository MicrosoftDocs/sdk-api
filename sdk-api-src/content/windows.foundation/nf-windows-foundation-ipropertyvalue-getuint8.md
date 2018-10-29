---
UID: NF:windows.foundation.IPropertyValue.GetUInt8
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the unsigned 8-bit integer value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getuint8.htm
tech.root: WinRT
ms.assetid: 736B44FF-F5A7-463A-9892-399CB3EC90B4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetUInt8, GetUInt8 method [Windows Runtime], GetUInt8 method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetUInt8 method, IPropertyValue.GetUInt8, IPropertyValue.IPropertyValue, IPropertyValue::GetUInt8, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetUInt8, winrt.ipropertyvalue_getuint8
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
 - IPropertyValue.GetUInt8
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the unsigned 8-bit integer value that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param value [out, retval]

Type: <b>BYTE*</b>

The unsigned 8-bit integer values.


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



<a href="https://msdn.microsoft.com/8CDCDB96-7E77-4B63-8417-D669ED4850BF">IPropertyValueStatics::CreateUInt8</a>
 

 

