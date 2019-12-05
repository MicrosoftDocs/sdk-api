---
UID: NF:windows.foundation.IPropertyValue.GetBoolean
title: IPropertyValue::IPropertyValue (windows.foundation.h)
description: Gets the 8-bit Boolean value that is stored in the current IPropertyValue object.
old-location: winrt\ipropertyvalue_getboolean.htm
tech.root: WinRT
ms.assetid: 5877E4BD-5712-4426-A31F-079E16ED0B4A
ms.date: 12/05/2018
ms.keywords: GetBoolean, GetBoolean method [Windows Runtime], GetBoolean method [Windows Runtime],IPropertyValue interface, IPropertyValue interface [Windows Runtime],GetBoolean method, IPropertyValue.GetBoolean, IPropertyValue.IPropertyValue, IPropertyValue::GetBoolean, IPropertyValue::IPropertyValue, windows/IPropertyValue::GetBoolean, winrt.ipropertyvalue_getboolean
ms.topic: method
f1_keywords:
- windows.foundation/IPropertyValue.GetBoolean
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyValue::IPropertyValue


## -description


Gets the 8-bit Boolean value that is stored in the current <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a> object.


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
The type of <i>value</i> does not match the value of the <a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvalue-get_type">Type</a> property.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nf-windows-foundation-ipropertyvaluestatics-createboolean">CreateBoolean</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.foundation/nn-windows-foundation-ipropertyvalue">IPropertyValue</a>
 

 

