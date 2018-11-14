---
UID: NF:windows.foundation.IPropertyValueStatics.CreateUInt64
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-sdk-content
description: Creates a new IPropertyValue object that contains the specified unsigned 64-bit integer value.
old-location: winrt\ipropertyvaluestatics_createuint64.htm
tech.root: WinRT
ms.assetid: 49158177-D74E-4310-984D-A1C511840EF9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateUInt64, CreateUInt64 method [Windows Runtime], CreateUInt64 method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateUInt64 method, IPropertyValueStatics.CreateUInt64, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateUInt64, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateUInt64, winrt.ipropertyvaluefactory_createuint64, winrt.ipropertyvaluestatics_createuint64
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
 - IPropertyValueStatics.CreateUInt64
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
- IPropertyValueStatics.CreateUInt64
: 
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified unsigned 64-bit integer value.


## -parameters




### -param value [in]

Type: <b>UINT64</b>

The unsigned 64-bit integer value to store.


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



Use the <b>CreateUInt64</b> method to  store a value in an <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object. You can add the  <b>IPropertyValue</b> object to a property store. Use the <a href="https://msdn.microsoft.com/2FD209CA-9A8D-40F3-B82E-E80A7D212A5D">GetUInt64</a> method to retrieve the value from the  <b>IPropertyValue</b> object.




## -see-also




<a href="https://msdn.microsoft.com/2FD209CA-9A8D-40F3-B82E-E80A7D212A5D">IPropertyValue::GetUInt64</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

