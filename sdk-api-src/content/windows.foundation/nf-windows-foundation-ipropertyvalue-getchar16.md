---
UID: NF:windows.foundation.IPropertyValue.GetChar16
title: IPropertyValue::GetChar16 method
author: windows-driver-content
description: Gets the Unicode character that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getchar16.htm
old-project: WinRT
ms.assetid: 46412359-A57E-489C-9992-5A30AB2DA8C4
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetChar16 method [Windows Runtime], GetChar16 method [Windows Runtime], IPropertyValue interface, GetChar16,IPropertyValue.GetChar16, IPropertyValue, IPropertyValue interface [Windows Runtime], GetChar16 method, IPropertyValue::GetChar16, windows/IPropertyValue::GetChar16, winrt.ipropertyvalue_getchar16
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windows.Foundation.h
api_name:
-	IPropertyValue.GetChar16
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValue::GetChar16 method


## -description


Gets the Unicode character that is stored in the current <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object.


## -parameters




### -param value [out, retval]

Type: <b>WCHAR*</b>

The Unicode character.


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
The type of <i>value</i> does not match the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a>



<a href="https://msdn.microsoft.com/E8400B85-029A-4E9A-963B-CC3012B7BE7F">IPropertyValueStatics::CreateChar16</a>
 

 

