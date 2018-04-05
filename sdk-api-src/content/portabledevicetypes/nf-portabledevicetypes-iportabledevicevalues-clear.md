---
UID: NF:portabledevicetypes.IPortableDeviceValues.Clear
title: IPortableDeviceValues::Clear method
author: windows-driver-content
description: The Clear method deletes all items from the collection.
old-location: wpdsdk\iportabledevicevalues_clear.htm
old-project: wpd_sdk
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Clear method [Windows Portable Devices SDK], Clear method [Windows Portable Devices SDK], IPortableDeviceValues interface, Clear,IPortableDeviceValues.Clear, IPortableDeviceValues, IPortableDeviceValues interface [Windows Portable Devices SDK], Clear method, IPortableDeviceValues::Clear, IPortableDeviceValuesClear, portabledevicetypes/IPortableDeviceValues::Clear, wpdsdk.iportabledevicevalues_clear
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
-	IPortableDeviceValues.Clear
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceValues::Clear method


## -description



The <b>Clear</b> method deletes all items from the collection.




## -parameters






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



This method frees the memory for all dynamically allocated items in the collection. For interfaces, it calls <b>Release</b>.




## -see-also




<a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues Interface</a>
 

 

