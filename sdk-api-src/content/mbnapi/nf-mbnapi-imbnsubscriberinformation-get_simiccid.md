---
UID: NF:mbnapi.IMbnSubscriberInformation.get_SimIccID
title: IMbnSubscriberInformation::get_SimIccID (mbnapi.h)
description: The SIM International circuit card number (SimICCID) for the device.
helpviewer_keywords: ["IMbnSubscriberInformation interface [Microsoft Broadband Networks]","SimIccID property","IMbnSubscriberInformation.SimIccID","IMbnSubscriberInformation.get_SimIccID","IMbnSubscriberInformation::SimIccID","IMbnSubscriberInformation::get_SimIccID","SimIccID property [Microsoft Broadband Networks]","SimIccID property [Microsoft Broadband Networks]","IMbnSubscriberInformation interface","get_SimIccID","mbn.imbnsubscriberinformation_simiccid","mbnapi/IMbnSubscriberInformation::SimIccID","mbnapi/IMbnSubscriberInformation::get_SimIccID"]
old-location: mbn\imbnsubscriberinformation_simiccid.htm
tech.root: mbn
ms.assetid: 18132836-65e8-4372-bfcd-ba0115b2d4d0
ms.date: 12/05/2018
ms.keywords: IMbnSubscriberInformation interface [Microsoft Broadband Networks],SimIccID property, IMbnSubscriberInformation.SimIccID, IMbnSubscriberInformation.get_SimIccID, IMbnSubscriberInformation::SimIccID, IMbnSubscriberInformation::get_SimIccID, SimIccID property [Microsoft Broadband Networks], SimIccID property [Microsoft Broadband Networks],IMbnSubscriberInformation interface, get_SimIccID, mbn.imbnsubscriberinformation_simiccid, mbnapi/IMbnSubscriberInformation::SimIccID, mbnapi/IMbnSubscriberInformation::get_SimIccID
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
 - IMbnSubscriberInformation::get_SimIccID
 - mbnapi/IMbnSubscriberInformation::get_SimIccID
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
 - IMbnSubscriberInformation.SimIccID
 - IMbnSubscriberInformation.get_SimIccID
---

# IMbnSubscriberInformation::get_SimIccID


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The SIM International circuit card number (SimICCID) for the device.

This property is read-only.

## -parameters

## -remarks

The International Circuit Card Id of the SIM varies between 15 to 20 digits in length and is represented in characters. This value is available only when the ready state of the device is <b>MBN_READY_STATE_INITIALIZED</b>. In some cases, it may also be populated in states such as <b>MBN_READY_STATE_DEVICE_LOCKED</b>, <b>MBN_READY_STATE_BAD_SIM</b>,  and <b>MBN_READY_STATE_FAILURE</b>. When this information is not available it is returned as an empty string.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsubscriberinformation">IMbnSubscriberInformation</a>