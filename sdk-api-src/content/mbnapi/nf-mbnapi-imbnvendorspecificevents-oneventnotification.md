---
UID: NF:mbnapi.IMbnVendorSpecificEvents.OnEventNotification
title: IMbnVendorSpecificEvents::OnEventNotification (mbnapi.h)
description: Notification method signaling a change event from the underlying Mobile Broadband device miniport driver.
helpviewer_keywords: ["IMbnVendorSpecificEvents interface [Microsoft Broadband Networks]","OnEventNotification method","IMbnVendorSpecificEvents.OnEventNotification","IMbnVendorSpecificEvents::OnEventNotification","OnEventNotification","OnEventNotification method [Microsoft Broadband Networks]","OnEventNotification method [Microsoft Broadband Networks]","IMbnVendorSpecificEvents interface","mbn.imbnvendorspecificevents_oneventnotification","mbnapi/IMbnVendorSpecificEvents::OnEventNotification"]
old-location: mbn\imbnvendorspecificevents_oneventnotification.htm
tech.root: mbn
ms.assetid: c3d10e9c-b60f-42e8-adaa-2c0ba3c77718
ms.date: 12/05/2018
ms.keywords: IMbnVendorSpecificEvents interface [Microsoft Broadband Networks],OnEventNotification method, IMbnVendorSpecificEvents.OnEventNotification, IMbnVendorSpecificEvents::OnEventNotification, OnEventNotification, OnEventNotification method [Microsoft Broadband Networks], OnEventNotification method [Microsoft Broadband Networks],IMbnVendorSpecificEvents interface, mbn.imbnvendorspecificevents_oneventnotification, mbnapi/IMbnVendorSpecificEvents::OnEventNotification
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IMbnVendorSpecificEvents::OnEventNotification
 - mbnapi/IMbnVendorSpecificEvents::OnEventNotification
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
 - IMbnVendorSpecificEvents.OnEventNotification
---

# IMbnVendorSpecificEvents::OnEventNotification


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method signaling a change event from the underlying Mobile Broadband device miniport driver.

## -parameters

### -param vendorOperation [in]

A <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificoperation">IMbnVendorSpecificOperation</a> interface representing the device on which the event has occurred.

### -param vendorSpecificData [in]

A byte array containing the data returned by underlying miniport driver.

## -returns

This method must return <b>S_OK</b>.

## -remarks

This byte array contains the byte by byte copy of data returned by underlying miniport driver.  The Mobile Broadband service will free the memory for this field after the function call returns. If an application wants to use this data then it should copy the contents in its own memory.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnvendorspecificevents">IMbnVendorSpecificEvents</a>