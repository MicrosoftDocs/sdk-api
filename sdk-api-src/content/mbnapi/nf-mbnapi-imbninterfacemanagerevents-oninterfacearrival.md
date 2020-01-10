---
UID: NF:mbnapi.IMbnInterfaceManagerEvents.OnInterfaceArrival
title: IMbnInterfaceManagerEvents::OnInterfaceArrival (mbnapi.h)
description: Notification method that signals that a device has been added to the system.
old-location: mbn\imbninterfacemanagerevents_oninterfacearrival.htm
tech.root: mbn
ms.assetid: 1a65aed6-34d4-420b-b175-a2a778712771
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks],OnInterfaceArrival method, IMbnInterfaceManagerEvents.OnInterfaceArrival, IMbnInterfaceManagerEvents::OnInterfaceArrival, OnInterfaceArrival, OnInterfaceArrival method [Microsoft Broadband Networks], OnInterfaceArrival method [Microsoft Broadband Networks],IMbnInterfaceManagerEvents interface, mbn.imbninterfacemanagerevents_oninterfacearrival, mbnapi/IMbnInterfaceManagerEvents::OnInterfaceArrival
f1_keywords:
- mbnapi/IMbnInterfaceManagerEvents.OnInterfaceArrival
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
- IMbnInterfaceManagerEvents.OnInterfaceArrival
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceManagerEvents::OnInterfaceArrival


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that signals that a device has been added to the system.


## -parameters




### -param newInterface [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the new device.


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanagerevents">IMbnInterfaceManagerEvents</a>
 

 

