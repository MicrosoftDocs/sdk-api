---
UID: NC:bluetoothapis.PFN_AUTHENTICATION_CALLBACK_EX
title: PFN_AUTHENTICATION_CALLBACK_EX (bluetoothapis.h)
description: PFN_AUTHENTICATION_CALLBACK_EX function is a callback function prototype used in conjunction with the BluetoothRegisterForAuthenticationEx function.
helpviewer_keywords: ["PFN_AUTHENTICATION_CALLBACK_EX","PFN_AUTHENTICATION_CALLBACK_EX callback","PFN_AUTHENTICATION_CALLBACK_EX callback function [Bluetooth]","bluetooth.pfn_authentication_callback_ex","bluetoothapis/PFN_AUTHENTICATION_CALLBACK_EX"]
old-location: bluetooth\pfn_authentication_callback_ex.htm
tech.root: bluetooth
ms.assetid: 835a624f-c08d-402c-940b-4443e1b38d58
ms.date: 12/05/2018
ms.keywords: PFN_AUTHENTICATION_CALLBACK_EX, PFN_AUTHENTICATION_CALLBACK_EX callback, PFN_AUTHENTICATION_CALLBACK_EX callback function [Bluetooth], bluetooth.pfn_authentication_callback_ex, bluetoothapis/PFN_AUTHENTICATION_CALLBACK_EX
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - PFN_AUTHENTICATION_CALLBACK_EX
 - bluetoothapis/PFN_AUTHENTICATION_CALLBACK_EX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - BluetoothAPIs.h
api_name:
 - PFN_AUTHENTICATION_CALLBACK_EX
---

# PFN_AUTHENTICATION_CALLBACK_EX callback function


## -description

The <i>PFN_AUTHENTICATION_CALLBACK_EX</i> function is a callback function prototype  used in conjunction with the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthenticationex">BluetoothRegisterForAuthenticationEx</a> function.
<div class="alert"><b>Note</b>  This structure is supported in Windows Vista SP2 and Windows 7.</div><div> </div>

## -parameters

### -param pvParam [in, optional]

Optional. A context pointer previously passed into the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a> function.

### -param pAuthCallbackParams [in]

A <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_authentication_callback_params">BLUETOOTH_AUTHENTICATION_CALLBACK_PARAMS</a> structure that contains device and authentication configuration information specific to the Bluetooth device responding to an authentication request.

## -returns

The return value from this function is ignored by the system.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthenticationex">BluetoothRegisterForAuthenticationEx</a>



<a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_authentication_callback">PFN_AUTHENTICATION_CALLBACK</a>