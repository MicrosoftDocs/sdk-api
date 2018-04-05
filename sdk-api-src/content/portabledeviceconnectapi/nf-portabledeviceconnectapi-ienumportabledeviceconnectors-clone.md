---
UID: NF:portabledeviceconnectapi.IEnumPortableDeviceConnectors.Clone
title: IEnumPortableDeviceConnectors::Clone method
author: windows-driver-content
description: Creates a copy of the current IEnumPortableDeviceConnectors interface.
old-location: wpdsdk\ienumportabledeviceconnectors_clone.htm
old-project: wpd_sdk
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Clone method [Windows Portable Devices SDK], Clone method [Windows Portable Devices SDK], IEnumPortableDeviceConnectors interface, Clone,IEnumPortableDeviceConnectors.Clone, IEnumPortableDeviceConnectors, IEnumPortableDeviceConnectors interface [Windows Portable Devices SDK], Clone method, IEnumPortableDeviceConnectors::Clone, devpkey/IEnumPortableDeviceConnectors::Clone, portabledeviceconnectapi/IEnumPortableDeviceConnectors::Clone, wpdsdk.ienumportabledeviceconnectors_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
-	IEnumPortableDeviceConnectors.Clone
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IEnumPortableDeviceConnectors::Clone method


## -description


The <b>Clone</b> method creates a copy of the current <a href="https://msdn.microsoft.com/99aa1e89-5e20-4f6e-82b5-acf63305eba0">IEnumPortableDeviceConnectors</a> interface.


## -parameters




### -param ppEnum [out]

The address of a pointer to an <a href="https://msdn.microsoft.com/99aa1e89-5e20-4f6e-82b5-acf63305eba0">IEnumPortableDeviceConnectors</a> interface.  The calling application must release this interface when it is done with it.


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




<a href="https://msdn.microsoft.com/99aa1e89-5e20-4f6e-82b5-acf63305eba0">IEnumPortableDeviceConnectors</a>
 

 

