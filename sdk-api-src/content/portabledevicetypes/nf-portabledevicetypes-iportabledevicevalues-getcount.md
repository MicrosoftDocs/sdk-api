---
UID: NF:portabledevicetypes.IPortableDeviceValues.GetCount
title: IPortableDeviceValues::GetCount method
author: windows-driver-content
description: The GetCount method retrieves the number of items in the collection.
old-location: wpdsdk\iportabledevicevalues_getcount.htm
old-project: wpd_sdk
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetCount method [Windows Portable Devices SDK], GetCount method [Windows Portable Devices SDK], IPortableDeviceValues interface, GetCount,IPortableDeviceValues.GetCount, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], GetCount method, IPortableDeviceValues::GetCount, IPortableDeviceValuesGetCount, portabledevicetypes/IPortableDeviceValues::GetCount, wpdsdk.iportabledevicevalues_getcount
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
-	IPortableDeviceValues.GetCount
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::GetCount method


## -description



The <b>GetCount</b> method retrieves the number of items in the collection.




## -parameters




### -param pcelt [in]

Pointer to a <b>DWORD</b> that contains the number of items in the collection.


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
 




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>
 

 

