---
UID: NF:windows.foundation.IPropertyValue.GetBoolean
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the 8-bit Boolean value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getboolean.htm
tech.root: WinRT
ms.assetid: 5877E4BD-5712-4426-A31F-079E16ED0B4A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetBoolean, GetBoolean method [Windows Runtime], GetBoolean method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetBoolean method, IPropertyValue.GetBoolean, IPropertyValue.IPropertyValue, IPropertyValue::GetBoolean, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetBoolean, winrt.ipropertyvalue_getboolean
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
 - IPropertyValue.GetBoolean
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the 8-bit Boolean value that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param value [out, retval]

Type: <b>BOOLEAN*</b>

The 8-bit Boolean value.


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
The type of <i>value</i> does not match the value of the <a href="https://msdn.microsoft.com/8C6C042A-53AA-439B-8D8D-F67DB45CC3C6">Type</a> property.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/F825D8F2-8FCE-48A7-9BD8-57E5D97A0E88">CreateBoolean</a>



<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>
 

 

