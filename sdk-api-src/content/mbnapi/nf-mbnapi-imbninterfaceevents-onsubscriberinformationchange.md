---
UID: NF:mbnapi.IMbnInterfaceEvents.OnSubscriberInformationChange
title: IMbnInterfaceEvents::OnSubscriberInformationChange (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate that the subscriber information for the device has changed.
helpviewer_keywords: ["IMbnInterfaceEvents interface [Microsoft Broadband Networks]","OnSubscriberInformationChange method","IMbnInterfaceEvents.OnSubscriberInformationChange","IMbnInterfaceEvents::OnSubscriberInformationChange","OnSubscriberInformationChange","OnSubscriberInformationChange method [Microsoft Broadband Networks]","OnSubscriberInformationChange method [Microsoft Broadband Networks]","IMbnInterfaceEvents interface","mbn.imbninterfaceevents_onsubscriberinformationchange","mbnapi/IMbnInterfaceEvents::OnSubscriberInformationChange"]
old-location: mbn\imbninterfaceevents_onsubscriberinformationchange.htm
tech.root: mbn
ms.assetid: 26d4fbdb-9c13-4934-a6bb-df581d0c18e9
ms.date: 12/05/2018
ms.keywords: IMbnInterfaceEvents interface [Microsoft Broadband Networks],OnSubscriberInformationChange method, IMbnInterfaceEvents.OnSubscriberInformationChange, IMbnInterfaceEvents::OnSubscriberInformationChange, OnSubscriberInformationChange, OnSubscriberInformationChange method [Microsoft Broadband Networks], OnSubscriberInformationChange method [Microsoft Broadband Networks],IMbnInterfaceEvents interface, mbn.imbninterfaceevents_onsubscriberinformationchange, mbnapi/IMbnInterfaceEvents::OnSubscriberInformationChange
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
 - IMbnInterfaceEvents::OnSubscriberInformationChange
 - mbnapi/IMbnInterfaceEvents::OnSubscriberInformationChange
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
 - IMbnInterfaceEvents.OnSubscriberInformationChange
---

# IMbnInterfaceEvents::OnSubscriberInformationChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate that the subscriber information for the device has changed.

## -parameters

### -param newInterface [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> that represents a device on which the subscriber information has changed.

## -returns

This method must return <b>S_OK</b>.

## -remarks

The application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getsubscriberinformation">GetSubscriberInformation</a> method of the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a> to get new subscriber information.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterfaceevents">IMbnInterfaceEvents</a>