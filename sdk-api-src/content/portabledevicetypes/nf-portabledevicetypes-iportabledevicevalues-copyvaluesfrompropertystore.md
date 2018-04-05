---
UID: NF:portabledevicetypes.IPortableDeviceValues.CopyValuesFromPropertyStore
title: IPortableDeviceValues::CopyValuesFromPropertyStore method
author: windows-driver-content
description: The CopyValuesFromPropertyStore method copies the contents of an IPropertyStore into the collection.
old-location: wpdsdk\iportabledevicevalues_copyvaluesfrompropertystore.htm
old-project: wpd_sdk
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CopyValuesFromPropertyStore method [Windows Portable Devices SDK], CopyValuesFromPropertyStore method [Windows Portable Devices SDK], IPortableDeviceValues interface, CopyValuesFromPropertyStore,IPortableDeviceValues.CopyValuesFromPropertyStore, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], CopyValuesFromPropertyStore method, IPortableDeviceValues::CopyValuesFromPropertyStore, IPortableDeviceValuesCopyValuesFromPropertyStore, portabledevicetypes/IPortableDeviceValues::CopyValuesFromPropertyStore, wpdsdk.iportabledevicevalues_copyvaluesfrompropertystore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledevicetypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_STREAM_UNITS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceValues.CopyValuesFromPropertyStore
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::CopyValuesFromPropertyStore method


## -description



The <b>CopyValuesFromPropertyStore</b> method copies the contents of an <b>IPropertyStore</b> into the collection.




## -parameters




### -param pStore [in]

Pointer to an <b>IPropertyStore</b> to copy into the collection.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method automatically converts all <b>VT_BSTR</b> values to <b>VT_LPWSTR</b> values.

Many external applications or components that communicate with your application, such as some shell applications, use the <b>IPropertyStore</b> interface. This method provides a quick and easy way to exchange data with these programs.

This method is supported in Windows Vista and later versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/417a8723-fa46-44c8-9bdc-412c0f20969a">IPortableDeviceValues::CopyValuesToPropertyStore</a>
 

 

