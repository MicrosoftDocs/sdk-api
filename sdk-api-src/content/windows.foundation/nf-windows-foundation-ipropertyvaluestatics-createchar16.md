---
UID: NF:windows.foundation.IPropertyValueStatics.CreateChar16
title: IPropertyValueStatics::IPropertyValueStatics (windows.foundation.h)
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified Unicode character.
old-location: winrt\ipropertyvaluestatics_createchar16.htm
tech.root: WinRT
ms.assetid: E8400B85-029A-4E9A-963B-CC3012B7BE7F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateChar16, CreateChar16 method [Windows Runtime], CreateChar16 method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateChar16 method, IPropertyValueStatics.CreateChar16, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateChar16, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateChar16, winrt.ipropertyvaluefactory_createchar16, winrt.ipropertyvaluestatics_createchar16
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
 - IPropertyValueStatics.CreateChar16
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified Unicode character.


## -parameters




### -param value [in]

Type: <b>WCHAR</b>

The Unicode character to store.


### -param propertyValue [out, retval]

Type: <b><a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>**</b>

A pointer to a new object that contains <i>value</i>. Use the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method to get the <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> interface for the object.


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
The  property value was created successfully.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object could not be created.

</td>
</tr>
</table>
 




## -remarks



Use the <b>CreateChar16</b> method to  store a value in an <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object. You can add the  <b>IPropertyValue</b> object to a property store. Use the <a href="https://msdn.microsoft.com/46412359-A57E-489C-9992-5A30AB2DA8C4">GetChar16</a> method to retrieve the value from the  <b>IPropertyValue</b> object.




## -see-also




<a href="https://msdn.microsoft.com/46412359-A57E-489C-9992-5A30AB2DA8C4">IPropertyValue::GetChar16</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

