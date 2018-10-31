---
UID: NF:windows.foundation.IPropertyValue.GetDouble
title: IPropertyValue::IPropertyValue
author: windows-sdk-content
description: Gets the 64-bit floating point value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getdouble.htm
tech.root: WinRT
ms.assetid: 93EC7793-DAEF-4E1D-A9B8-2D79A3CBBBDC
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDouble, GetDouble method [Windows Runtime], GetDouble method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetDouble method, IPropertyValue.GetDouble, IPropertyValue.IPropertyValue, IPropertyValue::GetDouble, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetDouble, winrt.ipropertyvalue_getdouble
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
 - IPropertyValue.GetDouble
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValue::IPropertyValue


## -description


Gets the 64-bit floating point value that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


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
The type of <i>value</i> does not match the <a href="https://msdn.microsoft.com/8C6C042A-53AA-439B-8D8D-F67DB45CC3C6">Type</a> property.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/66BB900A-797A-4589-AB9F-C35371F2671E">IPropertyValueStatics::CreateDouble</a>
 

 

