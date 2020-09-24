---
UID: NF:mbnapi.IMbnSubscriberInformation.get_TelephoneNumbers
title: IMbnSubscriberInformation::get_TelephoneNumbers (mbnapi.h)
description: The telephone numbers associated with the device.
helpviewer_keywords: ["IMbnSubscriberInformation interface [Microsoft Broadband Networks]","TelephoneNumbers property","IMbnSubscriberInformation.TelephoneNumbers","IMbnSubscriberInformation.get_TelephoneNumbers","IMbnSubscriberInformation::TelephoneNumbers","IMbnSubscriberInformation::get_TelephoneNumbers","TelephoneNumbers property [Microsoft Broadband Networks]","TelephoneNumbers property [Microsoft Broadband Networks]","IMbnSubscriberInformation interface","get_TelephoneNumbers","mbn.imbnsubscriberinformation_telephonenumbers","mbnapi/IMbnSubscriberInformation::TelephoneNumbers","mbnapi/IMbnSubscriberInformation::get_TelephoneNumbers"]
old-location: mbn\imbnsubscriberinformation_telephonenumbers.htm
tech.root: mbn
ms.assetid: 0f50735e-e57b-4724-8754-1fc4a5634cb3
ms.date: 12/05/2018
ms.keywords: IMbnSubscriberInformation interface [Microsoft Broadband Networks],TelephoneNumbers property, IMbnSubscriberInformation.TelephoneNumbers, IMbnSubscriberInformation.get_TelephoneNumbers, IMbnSubscriberInformation::TelephoneNumbers, IMbnSubscriberInformation::get_TelephoneNumbers, TelephoneNumbers property [Microsoft Broadband Networks], TelephoneNumbers property [Microsoft Broadband Networks],IMbnSubscriberInformation interface, get_TelephoneNumbers, mbn.imbnsubscriberinformation_telephonenumbers, mbnapi/IMbnSubscriberInformation::TelephoneNumbers, mbnapi/IMbnSubscriberInformation::get_TelephoneNumbers
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
 - IMbnSubscriberInformation::get_TelephoneNumbers
 - mbnapi/IMbnSubscriberInformation::get_TelephoneNumbers
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
 - IMbnSubscriberInformation.TelephoneNumbers
 - IMbnSubscriberInformation.get_TelephoneNumbers
---

# IMbnSubscriberInformation::get_TelephoneNumbers


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The telephone numbers associated with the device.

This property is read-only.

## -parameters

## -remarks

This property provides the list of telephone numbers (TNs) assigned to the subscriber. In GSM the numbers are called Mobile Station ISDN Numbers (MSISDNs).  In CDMA they are called Mobile Directory Numbers (MDNs).

This value is not populated until the ready state reaches <b>MBN_READY_STATE_INITIALIZED</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnsubscriberinformation">IMbnSubscriberInformation</a>