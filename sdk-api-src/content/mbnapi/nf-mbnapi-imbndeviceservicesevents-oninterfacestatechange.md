---
UID: NF:mbnapi.IMbnDeviceServicesEvents.OnInterfaceStateChange
title: IMbnDeviceServicesEvents::OnInterfaceStateChange (mbnapi.h)
description: Notification method that signals a change in the state of device services on the system.
helpviewer_keywords: ["IMbnDeviceServicesEvents interface [Microsoft Broadband Networks]","OnInterfaceStateChange method","IMbnDeviceServicesEvents.OnInterfaceStateChange","IMbnDeviceServicesEvents::OnInterfaceStateChange","OnInterfaceStateChange","OnInterfaceStateChange method [Microsoft Broadband Networks]","OnInterfaceStateChange method [Microsoft Broadband Networks]","IMbnDeviceServicesEvents interface","mbn.imbndeviceservicesevents_oninterfacestatechange","mbnapi/IMbnDeviceServicesEvents::OnInterfaceStateChange"]
old-location: mbn\imbndeviceservicesevents_oninterfacestatechange.htm
tech.root: mbn
ms.assetid: 6677E80E-A9D1-45B5-AE3F-71EE22A7CCB6
ms.date: 12/05/2018
ms.keywords: IMbnDeviceServicesEvents interface [Microsoft Broadband Networks],OnInterfaceStateChange method, IMbnDeviceServicesEvents.OnInterfaceStateChange, IMbnDeviceServicesEvents::OnInterfaceStateChange, OnInterfaceStateChange, OnInterfaceStateChange method [Microsoft Broadband Networks], OnInterfaceStateChange method [Microsoft Broadband Networks],IMbnDeviceServicesEvents interface, mbn.imbndeviceservicesevents_oninterfacestatechange, mbnapi/IMbnDeviceServicesEvents::OnInterfaceStateChange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnDeviceServicesEvents::OnInterfaceStateChange
 - mbnapi/IMbnDeviceServicesEvents::OnInterfaceStateChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesEvents.OnInterfaceStateChange
---

# IMbnDeviceServicesEvents::OnInterfaceStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that signals a change in the state of device services on the system.

## -parameters

### -param interfaceID [in]

The <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-get_interfaceid">InterfaceID</a> of the device for which the device services state change notification is sent.

### -param stateChange [in]

A <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_device_services_interface_state">MBN_DEVICE_SERVICES_INTERFACE_STATE</a> enumeration that specifies whether the device service capable device is available or unavailable.

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

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicesevents">IMbnDeviceServicesEvents</a>