---
UID: NE:mbnapi.MBN_DEVICE_SERVICES_INTERFACE_STATE
title: MBN_DEVICE_SERVICES_INTERFACE_STATE (mbnapi.h)
author: windows-sdk-content
description: "."
old-location: mbn\mbn_device_services_interface_state.htm
tech.root: mbn
ms.assetid: 0EDED390-CB60-4D6C-9E62-87B3BF6F9050
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MBN_DEVICE_SERVICES_CAPABLE_INTERFACE_ARRIVAL, MBN_DEVICE_SERVICES_CAPABLE_INTERFACE_REMOVAL, MBN_DEVICE_SERVICES_INTERFACE_STATE, MBN_DEVICE_SERVICES_INTERFACE_STATE enumeration [Microsoft Broadband Networks], mbn.mbn_device_services_interface_state, mbnapi/MBN_DEVICE_SERVICES_CAPABLE_INTERFACE_ARRIVAL, mbnapi/MBN_DEVICE_SERVICES_CAPABLE_INTERFACE_REMOVAL, mbnapi/MBN_DEVICE_SERVICES_INTERFACE_STATE
ms.topic: enum
f1_keywords: 
 - "mbnapi/MBN_DEVICE_SERVICES_INTERFACE_STATE"
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
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_DEVICE_SERVICES_INTERFACE_STATE
targetos: Windows
req.typenames: MBN_DEVICE_SERVICES_INTERFACE_STATE
req.redist: 
ms.custom: 19H1
---

# MBN_DEVICE_SERVICES_INTERFACE_STATE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_DEVICE_SERVICES_INTERFACE_STATE</b> structure provides information about the state of device services capable Mobile Broadband devices.


## -enum-fields




### -field MBN_DEVICE_SERVICES_CAPABLE_INTERFACE_ARRIVAL

A Mobile Broadband device capable of supporting device service functionality has arrived.


### -field MBN_DEVICE_SERVICES_CAPABLE_INTERFACE_REMOVAL

A Mobile Broadband device capable of supporting device services functionality has been removed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicesevents-oninterfacestatechange">OnInterfaceStateChange</a>
 

 

