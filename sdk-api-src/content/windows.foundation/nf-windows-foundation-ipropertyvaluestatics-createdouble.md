---
UID: NF:windows.foundation.IPropertyValueStatics.CreateDouble
title: IPropertyValueStatics::IPropertyValueStatics
author: windows-driver-content
description: Creates a new IPropertyValue object that contains the specified 64-bit floating point value.
old-location: winrt\ipropertyvaluestatics_createdouble.htm
old-project: WinRT
ms.assetid: 66BB900A-797A-4589-AB9F-C35371F2671E
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: CreateDouble, CreateDouble method [Windows Runtime], CreateDouble method [Windows Runtime],IPropertyValueStatics interface, IPropertyValueStatics interface [Windows Runtime],CreateDouble method, IPropertyValueStatics.CreateDouble, IPropertyValueStatics.IPropertyValueStatics, IPropertyValueStatics::CreateDouble, IPropertyValueStatics::IPropertyValueStatics, windows/IPropertyValueStatics::CreateDouble, winrt.ipropertyvaluefactory_createdouble, winrt.ipropertyvaluestatics_createdouble
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
-	IPropertyValueStatics.CreateDouble
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IPropertyValueStatics::IPropertyValueStatics


## -description


Creates a new <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object that contains  the specified 64-bit floating point value.


## -parameters




### -param value [in]

Type: <b>DOUBLE</b>

The 64-bit floating point value to store.


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



Use the <b>CreateDouble</b> method to  store a value in an <a href="https://msdn.microsoft.com/447625BA-F982-4155-9B05-E478E1229443">IPropertyValue</a> object. You can add the  <b>IPropertyValue</b> object to a property store. Use the <a href="https://msdn.microsoft.com/93EC7793-DAEF-4E1D-A9B8-2D79A3CBBBDC">GetDouble</a> method to retrieve the value from the  <b>IPropertyValue</b> object.




## -see-also




<a href="https://msdn.microsoft.com/93EC7793-DAEF-4E1D-A9B8-2D79A3CBBBDC">IPropertyValue::GetDouble</a>



<a href="https://msdn.microsoft.com/946BD4F9-318C-4452-AEDB-DF2212A2D3CA">IPropertyValueStatics</a>
 

 

