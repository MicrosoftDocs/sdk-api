---
UID: NF:mbnapi.IMbnInterfaceEvents.OnEmergencyModeChange
title: IMbnInterfaceEvents::OnEmergencyModeChange (mbnapi.h)

description: This notification method is called by the Mobile Broadband service to indicate that the emergency mode has changed.
old-location: mbn\imbninterfaceevents_onemergencymodechange.htm
tech.root: mbn
ms.assetid: 637e0f6b-102f-436c-b0ec-edef16245675

ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnEmergencyModeChange method, IMbnInterfaceEvents.OnEmergencyModeChange, IMbnInterfaceEvents::OnEmergencyModeChange, OnEmergencyModeChange, OnEmergencyModeChange method [Microsoft Broadband Networks], OnEmergencyModeChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onemergencymodechange, mbnapi/IMbnInterfaceEvents::OnEmergencyModeChange
ms.topic: method
f1_keywords: 
 - "mbnapi/IMbnInterfaceEvents.OnEmergencyModeChange"
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
 - IMbnInterfaceEvents.OnEmergencyModeChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnInterfaceEvents::OnEmergencyModeChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate that the emergency mode has changed.


## -parameters




### -param newInterface [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device whose emergency mode has changed.  


## -returns



This method must return <b>S_OK</b>.




## -remarks



An application can call the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-inemergencymode">InEmergencyMode</a> method of the passed <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get the new emergency mode of the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>
 

 

