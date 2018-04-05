---
UID: NF:portabledeviceconnectapi.IEnumPortableDeviceConnectors.Skip
title: IEnumPortableDeviceConnectors::Skip method
author: windows-driver-content
description: Skips the specified number of devices in the enumeration sequence.
old-location: wpdsdk\ienumportabledeviceconnectors_skip.htm
old-project: wpd_sdk
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IEnumPortableDeviceConnectors, IEnumPortableDeviceConnectors interface [Windows Portable Devices SDK], Skip method, IEnumPortableDeviceConnectors::Skip, Skip method [Windows Portable Devices SDK], Skip method [Windows Portable Devices SDK], IEnumPortableDeviceConnectors interface, Skip,IEnumPortableDeviceConnectors.Skip, devpkey/IEnumPortableDeviceConnectors::Skip, portabledeviceconnectapi/IEnumPortableDeviceConnectors::Skip, wpdsdk.ienumportabledeviceconnectors_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGuids.lib
-	PortableDeviceGuids.dll
api_name:
-	IEnumPortableDeviceConnectors.Skip
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumPortableDeviceConnectors::Skip method


## -description


The <b>Skip</b> method skips the specified number of devices in the enumeration sequence.


## -parameters




### -param cConnectors [in]

The number of devices to skip.


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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified number of devices could not be skipped. One possible cause: The <i>cConnectors</i> parameter specifies more devices than actually remain in the enumeration sequence.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/99aa1e89-5e20-4f6e-82b5-acf63305eba0">IEnumPortableDeviceConnectors</a>
 

 

