---
UID: NE:mbnapi.MBN_READY_STATE
title: MBN_READY_STATE (mbnapi.h)
description: The MBN_READY_STATE enumerated type contains values that indicate the readiness of a Mobile Broadband device to engage in cellular network traffic operations.
helpviewer_keywords: ["MBN_READY_STATE","MBN_READY_STATE enumeration [Microsoft Broadband Networks]","MBN_READY_STATE_BAD_SIM","MBN_READY_STATE_DEVICE_BLOCKED","MBN_READY_STATE_DEVICE_LOCKED","MBN_READY_STATE_FAILURE","MBN_READY_STATE_INITIALIZED","MBN_READY_STATE_NOT_ACTIVATED","MBN_READY_STATE_OFF","MBN_READY_STATE_SIM_NOT_INSERTED","mbn.mbn_ready_state","mbnapi/MBN_READY_STATE","mbnapi/MBN_READY_STATE_BAD_SIM","mbnapi/MBN_READY_STATE_DEVICE_BLOCKED","mbnapi/MBN_READY_STATE_DEVICE_LOCKED","mbnapi/MBN_READY_STATE_FAILURE","mbnapi/MBN_READY_STATE_INITIALIZED","mbnapi/MBN_READY_STATE_NOT_ACTIVATED","mbnapi/MBN_READY_STATE_OFF","mbnapi/MBN_READY_STATE_SIM_NOT_INSERTED"]
old-location: mbn\mbn_ready_state.htm
tech.root: mbn
ms.assetid: 4f712cdc-ee9c-4ceb-9bc4-8a4fe19d0a37
ms.date: 12/05/2018
ms.keywords: MBN_READY_STATE, MBN_READY_STATE enumeration [Microsoft Broadband Networks], MBN_READY_STATE_BAD_SIM, MBN_READY_STATE_DEVICE_BLOCKED, MBN_READY_STATE_DEVICE_LOCKED, MBN_READY_STATE_FAILURE, MBN_READY_STATE_INITIALIZED, MBN_READY_STATE_NOT_ACTIVATED, MBN_READY_STATE_OFF, MBN_READY_STATE_SIM_NOT_INSERTED, mbn.mbn_ready_state, mbnapi/MBN_READY_STATE, mbnapi/MBN_READY_STATE_BAD_SIM, mbnapi/MBN_READY_STATE_DEVICE_BLOCKED, mbnapi/MBN_READY_STATE_DEVICE_LOCKED, mbnapi/MBN_READY_STATE_FAILURE, mbnapi/MBN_READY_STATE_INITIALIZED, mbnapi/MBN_READY_STATE_NOT_ACTIVATED, mbnapi/MBN_READY_STATE_OFF, mbnapi/MBN_READY_STATE_SIM_NOT_INSERTED
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
req.typenames: MBN_READY_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MBN_READY_STATE
 - mbnapi/MBN_READY_STATE
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
 - MBN_READY_STATE
---

# MBN_READY_STATE enumeration


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The <b>MBN_READY_STATE</b> enumerated type contains values that indicate the readiness of a Mobile Broadband device to engage in cellular network traffic operations.

  These values are returned by the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbninterface-getreadystate">GetReadyState</a> method of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>.  For a device with a SIM card, this is to signal that the SIM has been initialized and is ready for access.

## -enum-fields

### -field MBN_READY_STATE_OFF:0

The mobile broadband device stack is off.

### -field MBN_READY_STATE_INITIALIZED

The card and stack is powered up and ready to be used for mobile broadband operations.

### -field MBN_READY_STATE_SIM_NOT_INSERTED

The SIM is not inserted.

### -field MBN_READY_STATE_BAD_SIM

The SIM is invalid  (PIN Unblock Key retrials have exceeded the limit).

### -field MBN_READY_STATE_FAILURE

General device failure.

### -field MBN_READY_STATE_NOT_ACTIVATED

The subscription is not activated.

### -field MBN_READY_STATE_DEVICE_LOCKED

The device is locked by a PIN or password which is preventing the device from initializing and registering onto the network.  The calling application can call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpinmanager-getpinstate">GetPinState</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpinmanager">IMbnPinManager</a> interface to get the type of PIN needed to be entered to unlock the device.

### -field MBN_READY_STATE_DEVICE_BLOCKED

The device is blocked by a PIN or password which is preventing the device from initializing and registering onto the network.  The calling application should call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnpin-unblock">Unblock</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnpin">IMbnPin</a> interface to unblock the device.

### -field MBN_READY_STATE_NO_ESIM_PROFILE
