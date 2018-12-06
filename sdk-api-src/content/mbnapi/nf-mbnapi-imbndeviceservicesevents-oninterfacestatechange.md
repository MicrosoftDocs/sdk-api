---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnInterfaceStateChange
title: IMbnDeviceServicesEvents::OnInterfaceStateChange
author: windows-sdk-content
description: Notification method that signals a change in the state of device services on the system.
old-location: mbn\imbndeviceservicesevents_oninterfacestatechange.htm
tech.root: mbn
ms.assetid: 6677E80E-A9D1-45B5-AE3F-71EE22A7CCB6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnInterfaceStateChange method, IMbnDeviceServicesEvents.OnInterfaceStateChange, IMbnDeviceServicesEvents::OnInterfaceStateChange, OnInterfaceStateChange, OnInterfaceStateChange method [Microsoft Broadband Networks], OnInterfaceStateChange method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_oninterfacestatechange, mbnapi/IMbnDeviceServicesEvents::OnInterfaceStateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnDeviceServicesEvents.OnInterfaceStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnDeviceServicesEvents::OnInterfaceStateChange


## -description


Notification method that signals a change in the state of device services on the system.


## -parameters




### -param interfaceID [in]

The <a href="https://msdn.microsoft.com/9828567b-ef5e-44b7-90ce-1788cd8dd947">InterfaceID</a> of the device for which the device services state change notification is sent.


### -param stateChange [in]

A <a href="https://msdn.microsoft.com/0EDED390-CB60-4D6C-9E62-87B3BF6F9050">MBN_DEVICE_SERVICES_INTERFACE_STATE</a> enumeration that specifies whether the device service capable device is available or unavailable.


## -returns



The method must return the following value.

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
The method completed successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a>
 

 

