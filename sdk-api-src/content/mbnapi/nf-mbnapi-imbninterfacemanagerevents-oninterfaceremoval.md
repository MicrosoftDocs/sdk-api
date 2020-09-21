---
UID: NF:mbnapi.IMbnInterfaceManagerEvents.OnInterfaceRemoval
title: IMbnInterfaceManagerEvents::OnInterfaceRemoval (mbnapi.h)
description: Notification method that signals that a device has been removed from the system.
helpviewer_keywords: ["IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks]","OnInterfaceRemoval method","IMbnInterfaceManagerEvents.OnInterfaceRemoval","IMbnInterfaceManagerEvents::OnInterfaceRemoval","OnInterfaceRemoval","OnInterfaceRemoval method [Microsoft Broadband Networks]","OnInterfaceRemoval method [Microsoft Broadband Networks]","IMbnInterfaceManagerEvents interface","mbn.imbninterfacemanagerevents_oninterfaceremoval","mbnapi/IMbnInterfaceManagerEvents::OnInterfaceRemoval"]
old-location: mbn\imbninterfacemanagerevents_oninterfaceremoval.htm
tech.root: mbn
ms.assetid: d7c96d35-20e1-46e2-82db-4b1fc03cdd22
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceManagerEvents interface [Microsoft Broadband Networks],OnInterfaceRemoval method, IMbnInterfaceManagerEvents.OnInterfaceRemoval, IMbnInterfaceManagerEvents::OnInterfaceRemoval, OnInterfaceRemoval, OnInterfaceRemoval method [Microsoft Broadband Networks], OnInterfaceRemoval method [Microsoft Broadband Networks],IMbnInterfaceManagerEvents interface, mbn.imbninterfacemanagerevents_oninterfaceremoval, mbnapi/IMbnInterfaceManagerEvents::OnInterfaceRemoval
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnInterfaceManagerEvents::OnInterfaceRemoval
 - mbnapi/IMbnInterfaceManagerEvents::OnInterfaceRemoval
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
 - IMbnInterfaceManagerEvents.OnInterfaceRemoval
---

# IMbnInterfaceManagerEvents::OnInterfaceRemoval


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that signals that a device has been removed from the system.

## -parameters

### -param oldInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents the device that was removed.

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfacemanagerevents">IMbnInterfaceManagerEvents</a>