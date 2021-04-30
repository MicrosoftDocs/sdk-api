---
UID: NS:mbnapi.MBN_PIN_INFO
title: MBN_PIN_INFO (mbnapi.h)
description: The MBN_PIN_INFO structure represents the current PIN state of the device.
helpviewer_keywords: ["MBN_PIN_INFO","MBN_PIN_INFO structure [Microsoft Broadband Networks]","mbn.mbn_pin_info","mbnapi/MBN_PIN_INFO"]
old-location: mbn\mbn_pin_info.htm
tech.root: mbn
ms.assetid: c70b45ea-c16b-4d0d-946a-f543c827c458
ms.date: 12/05/2018
ms.keywords: MBN_PIN_INFO, MBN_PIN_INFO structure [Microsoft Broadband Networks], mbn.mbn_pin_info, mbnapi/MBN_PIN_INFO
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
req.typenames: MBN_PIN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PIN_INFO
 - mbnapi/MBN_PIN_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mbnapi.h
api_name:
 - MBN_PIN_INFO
---

# MBN_PIN_INFO structure


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PIN_INFO</b> structure represents the current PIN state of the device.  It indicates if some PIN is expected by the device and the PIN type expected.  Optionally, it also conveys remaining allowed attempts to enter a valid PIN.  This structure can be obtained by either calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> or supplied as an input parameter to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinevents-onentercomplete">OnEnterComplete</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinevents">IMbnPinEvents</a>.

## -struct-fields

### -field pinState

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_pin_state">MBN_PIN_STATE</a> value that indicates the current PIN state of the device.

### -field pinType

An <a href="/windows/desktop/api/mbnapi/ne-mbnapi-mbn_pin_type">MBN_PIN_TYPE</a> value that indicates the type of PIN expected.  This field is valid only when <b>pinState</b> is either <b>MBN_PIN_STATE_ENTER</b> or <b>MBN_PIN_STATE_UNBLOCK</b>.

### -field attemptsRemaining

Contains the number of attempts remaining to enter the valid PIN.  This information is not available on some devices.  If it is not available, then it is set to <b>MBN_ATTEMPTS_REMAINING_UNKNOWN</b>.