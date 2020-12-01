---
UID: NF:mbnapi.IMbnInterfaceEvents.OnScanNetworkComplete
title: IMbnInterfaceEvents::OnScanNetworkComplete (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate the completion of a network scan.
helpviewer_keywords: ["E_MBN_ALREADY_ACTIVE","E_MBN_DEVICE_BUSY","E_MBN_RADIO_POWER_OFF","IMbnInterfaceEvents interface [Microsoft Broadband Networks]","OnScanNetworkComplete method","IMbnInterfaceEvents.OnScanNetworkComplete","IMbnInterfaceEvents::OnScanNetworkComplete","OnScanNetworkComplete","OnScanNetworkComplete method [Microsoft Broadband Networks]","OnScanNetworkComplete method [Microsoft Broadband Networks]","IMbnInterfaceEvents interface","S_OK","mbn.imbninterfaceevents_onscannetworkcomplete","mbnapi/IMbnInterfaceEvents::OnScanNetworkComplete"]
old-location: mbn\imbninterfaceevents_onscannetworkcomplete.htm
tech.root: mbn
ms.assetid: 6320c76b-b8a6-44dc-88bb-e20a85d5cfca
ms.date: 11/19/2020
ms.keywords: E_MBN_ALREADY_ACTIVE, E_MBN_DEVICE_BUSY, E_MBN_RADIO_POWER_OFF, IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnScanNetworkComplete method, IMbnInterfaceEvents.OnScanNetworkComplete, IMbnInterfaceEvents::OnScanNetworkComplete, OnScanNetworkComplete, OnScanNetworkComplete method [Microsoft Broadband Networks], OnScanNetworkComplete method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, S_OK, mbn.imbninterfaceevents_onscannetworkcomplete, mbnapi/IMbnInterfaceEvents::OnScanNetworkComplete
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
 - IMbnInterfaceEvents::OnScanNetworkComplete
 - mbnapi/IMbnInterfaceEvents::OnScanNetworkComplete
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
 - IMbnInterfaceEvents.OnScanNetworkComplete
---

# IMbnInterfaceEvents::OnScanNetworkComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate the completion of a network scan.

## -parameters

### -param newInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents a device on which this operation was performed.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service for this notification.

### -param status [in]

The operation completion status



A calling application can expect one of the following values.


**S_OK**

The operation  was successful.


**E_MBN_RADIO_POWER_OFF**

Can't get a visible network list because the device radio is off.  The application can issue a network scan request when it gets the radio-turned-on notification.


**E_MBN_DEVICE_BUSY**

The device is busy and can't currently perform a network scan operation.  This is returned by devices which don't support a network scan operation when it has a data connection established.


**E_MBN_ALREADY_ACTIVE**

A network scan operation is already in progress.

## -returns

This method must return <b>S_OK</b>.

## -remarks

If the operation completed successfully, that is, when <i>status</i> is  S_OK,  the Mobile Broadband service successfully updated the cached list of visible providers.  An application can then call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getvisibleproviders">GetVisibleProviders</a> method of the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get the list of visible providers.

If multiple applications registered for notifications, then this method will be called on all registered applications. This means that an application that did not initiate the update operation will receive a notification.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>