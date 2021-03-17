---
UID: NF:mbnapi.IMbnSignalEvents.OnSignalStateChange
title: IMbnSignalEvents::OnSignalStateChange (mbnapi.h)
description: This notification method is called by the Mobile Broadband service to indicate that a signal quality update is available.
helpviewer_keywords: ["IMbnSignalEvents interface [Microsoft Broadband Networks]","OnSignalStateChange method","IMbnSignalEvents.OnSignalStateChange","IMbnSignalEvents::OnSignalStateChange","OnSignalStateChange","OnSignalStateChange method [Microsoft Broadband Networks]","OnSignalStateChange method [Microsoft Broadband Networks]","IMbnSignalEvents interface","mbn.imbnsignalevents_onsignalstatechange","mbnapi/IMbnSignalEvents::OnSignalStateChange"]
old-location: mbn\imbnsignalevents_onsignalstatechange.htm
tech.root: mbn
ms.assetid: 07e98555-03fa-4852-af65-55778dc9c477
ms.date: 12/05/2018
ms.keywords: IMbnSignalEvents interface [Microsoft Broadband Networks],OnSignalStateChange method, IMbnSignalEvents.OnSignalStateChange, IMbnSignalEvents::OnSignalStateChange, OnSignalStateChange, OnSignalStateChange method [Microsoft Broadband Networks], OnSignalStateChange method [Microsoft Broadband Networks],IMbnSignalEvents interface, mbn.imbnsignalevents_onsignalstatechange, mbnapi/IMbnSignalEvents::OnSignalStateChange
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
 - IMbnSignalEvents::OnSignalStateChange
 - mbnapi/IMbnSignalEvents::OnSignalStateChange
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
 - IMbnSignalEvents.OnSignalStateChange
---

# IMbnSignalEvents::OnSignalStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

This notification method is called by the Mobile Broadband service to indicate that a signal quality update is available.

## -parameters

### -param newInterface [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignal">IMbnSignal</a> interface  for which the signal quality update was received.

## -returns

This method must return <b>S_OK</b>.

## -remarks

<b>OnSignalStateChange</b> is called by the Mobile Broadband service to notify a calling application that a signal quality update is available.  This includes an update of the signal notification period, threshold for signal notification, signal strength received, and error rate in the received signal. 
An application can get updated values from the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignal">IMbnSignal</a> interface passed in this method.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsignalevents">IMbnSignalEvents</a>