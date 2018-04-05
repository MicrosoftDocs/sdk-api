---
UID: NF:portabledevicetypes.IPortableDeviceValues.CopyValuesToPropertyStore
title: IPortableDeviceValues::CopyValuesToPropertyStore method
author: windows-driver-content
description: The CopyValuesToPropertyStore method copies all the values from a collection into an IPropertyStore interface.
old-location: wpdsdk\iportabledevicevalues_copyvaluestopropertystore.htm
old-project: wpd_sdk
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CopyValuesToPropertyStore method [Windows Portable Devices SDK], CopyValuesToPropertyStore method [Windows Portable Devices SDK], IPortableDeviceValues interface, CopyValuesToPropertyStore,IPortableDeviceValues.CopyValuesToPropertyStore, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], CopyValuesToPropertyStore method, IPortableDeviceValues::CopyValuesToPropertyStore, IPortableDeviceValuesCopyValuesToPropertyStore, portabledevicetypes/IPortableDeviceValues::CopyValuesToPropertyStore, wpdsdk.iportabledevicevalues_copyvaluestopropertystore
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
-	IPortableDeviceValues.CopyValuesToPropertyStore
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::CopyValuesToPropertyStore method


## -description



The <b>CopyValuesToPropertyStore</b> method copies all the values from a collection into an <b>IPropertyStore</b> interface.




## -parameters




### -param pStore [in]

Pointer to a store object.


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



This method does not convert values of VT_LPWSTR into VT_BSTR. Many external applications or components that communicate with your application, such as some shell applications, use the <b>IPropertyStore</b> interface. This method provides a quick and easy way to exchange data with these programs.

This method is supported in Windows Vista and later versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/887c9569-ff76-41cf-8782-62c59c04e831">IPortableDeviceValues::CopyValuesFromPropertyStore</a>
 

 

