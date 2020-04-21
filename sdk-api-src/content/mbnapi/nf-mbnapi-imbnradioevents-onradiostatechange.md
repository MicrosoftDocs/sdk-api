---
UID: NF:mbnapi.IMbnRadioEvents.OnRadioStateChange
title: IMbnRadioEvents::OnRadioStateChange (mbnapi.h)
description: A notification signaling that the radio state of the device has changed.helpviewer_keywords: ["IMbnRadioEvents interface [Microsoft Broadband Networks]","OnRadioStateChange method","IMbnRadioEvents.OnRadioStateChange","IMbnRadioEvents::OnRadioStateChange","OnRadioStateChange","OnRadioStateChange method [Microsoft Broadband Networks]","OnRadioStateChange method [Microsoft Broadband Networks]","IMbnRadioEvents interface","mbn.imbnradioevents_onradiostatechange","mbnapi/IMbnRadioEvents::OnRadioStateChange"]
old-location: mbn\imbnradioevents_onradiostatechange.htm
tech.root: mbn
ms.assetid: ae7bf0d0-333b-429d-9dd1-9580745aad35
ms.date: 12/05/2018
ms.keywords: IMbnRadioEvents interface [Microsoft Broadband Networks],OnRadioStateChange method, IMbnRadioEvents.OnRadioStateChange, IMbnRadioEvents::OnRadioStateChange, OnRadioStateChange, OnRadioStateChange method [Microsoft Broadband Networks], OnRadioStateChange method [Microsoft Broadband Networks],IMbnRadioEvents interface, mbn.imbnradioevents_onradiostatechange, mbnapi/IMbnRadioEvents::OnRadioStateChange
f1_keywords:
- mbnapi/IMbnRadioEvents.OnRadioStateChange
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnRadioEvents.OnRadioStateChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnRadioEvents::OnRadioStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

A notification signaling that the radio state of the device has changed.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnradio">IMbnRadio</a> interface representing the device for which the radio state has changed.


## -returns



This method must return <b>S_OK</b>.




## -remarks



New software and hardware radio states can be obtained from the passed <i>newInterface</i> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnradioevents">IMbnRadioEvents</a>
 

 

