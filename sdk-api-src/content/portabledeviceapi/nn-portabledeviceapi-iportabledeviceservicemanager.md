---
UID: NN:portabledeviceapi.IPortableDeviceServiceManager
title: IPortableDeviceServiceManager
author: windows-sdk-content
description: Retrieves the device associated with a service and the list of services found on a device.
old-location: wpdsdk\iportabledeviceservicemanager.htm
old-project: wpd_sdk
ms.assetid: 8df23343-26f0-4fb0-90b9-e8b75bcadffa
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDeviceServiceManager, IPortableDeviceServiceManager interface [Windows Portable Devices SDK], IPortableDeviceServiceManager interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceServiceManager, wpdsdk.iportabledeviceservicemanager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceServiceManager
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceServiceManager interface


## -description


The <b>IPortableDeviceServiceManager</b> interface retrieves the device associated with a service and the list of services found on a device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceServiceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceServiceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceServiceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cdb03fb-8cb2-4eee-af90-3aec0a055fc5">GetDeviceForService</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with the specified service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6b06f4d-c07e-4cd4-b96e-e8b9b4f98df8">GetDeviceServices</a>
</td>
<td align="left" width="63%">
Retrieves a list of the services associated with the specified device.

</td>
</tr>
</table> 

