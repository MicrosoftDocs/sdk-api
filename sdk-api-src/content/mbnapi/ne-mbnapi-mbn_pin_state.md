---
UID: NE:mbnapi.MBN_PIN_STATE
title: MBN_PIN_STATE (mbnapi.h)
description: The MBN_PIN_STATE enumerated type indicates the current PIN state of the Mobile Broadband device.
helpviewer_keywords: ["MBN_PIN_STATE","MBN_PIN_STATE enumeration [Microsoft Broadband Networks]","MBN_PIN_STATE_ENTER","MBN_PIN_STATE_NONE","MBN_PIN_STATE_UNBLOCK","mbn.mbn_pin_state","mbnapi/MBN_PIN_STATE","mbnapi/MBN_PIN_STATE_ENTER","mbnapi/MBN_PIN_STATE_NONE","mbnapi/MBN_PIN_STATE_UNBLOCK"]
old-location: mbn\mbn_pin_state.htm
tech.root: mbn
ms.assetid: 5e32e369-2e83-4682-a10c-718f228308ab
ms.date: 12/05/2018
ms.keywords: MBN_PIN_STATE, MBN_PIN_STATE enumeration [Microsoft Broadband Networks], MBN_PIN_STATE_ENTER, MBN_PIN_STATE_NONE, MBN_PIN_STATE_UNBLOCK, mbn.mbn_pin_state, mbnapi/MBN_PIN_STATE, mbnapi/MBN_PIN_STATE_ENTER, mbnapi/MBN_PIN_STATE_NONE, mbnapi/MBN_PIN_STATE_UNBLOCK
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
req.typenames: MBN_PIN_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_PIN_STATE
 - mbnapi/MBN_PIN_STATE
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
 - MBN_PIN_STATE
---

# MBN_PIN_STATE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_PIN_STATE</b> enumerated type indicates the current PIN state of the Mobile Broadband device.

## -enum-fields

### -field MBN_PIN_STATE_NONE:0

Indicates that no PIN is currently required.  

This state can occur when the device does not require a PIN.  It can also occur after repeated PIN entry attempts have exhausted the allowable quota and the device does not allow the PIN to be unblocked programmatically

### -field MBN_PIN_STATE_ENTER

Indicates that the device is currently locked and requires a PIN to be entered to unlock it  The caller can unlock the device by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-enter">Enter</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> interface.

### -field MBN_PIN_STATE_UNBLOCK

Indicates that the device is in a PIN blocked state and that the PIN needs to be unblocked using the corresponding PIN Unblock Key (PUK).  The caller can unlock the device by calling the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock">Unblock</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> interface.

This state can occur after repeated PIN entry attempts have exhausted the allowable quota.
