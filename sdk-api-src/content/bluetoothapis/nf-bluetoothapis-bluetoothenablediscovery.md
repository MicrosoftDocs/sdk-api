---
UID: NF:bluetoothapis.BluetoothEnableDiscovery
title: BluetoothEnableDiscovery function (bluetoothapis.h)
description: The BluetoothEnableDiscovery function changes the discovery state of a local Bluetooth radio or radios.
helpviewer_keywords: ["BluetoothEnableDiscovery","BluetoothEnableDiscovery function [Bluetooth]","bluetooth.bluetoothenablediscovery","bluetoothapis/BluetoothEnableDiscovery"]
old-location: bluetooth\bluetoothenablediscovery.htm
tech.root: bluetooth
ms.assetid: ca28c9cd-a271-48fa-901c-e99e063854d5
ms.date: 12/05/2018
ms.keywords: BluetoothEnableDiscovery, BluetoothEnableDiscovery function [Bluetooth], bluetooth.bluetoothenablediscovery, bluetoothapis/BluetoothEnableDiscovery
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
req.lib: Bthprops.lib
req.dll: bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothEnableDiscovery
 - bluetoothapis/BluetoothEnableDiscovery
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothEnableDiscovery
---

# BluetoothEnableDiscovery function


## -description

The <b>BluetoothEnableDiscovery</b> function changes the discovery state of a local Bluetooth radio or radios.

## -parameters

### -param hRadio

Valid local radio handle, or <b>NULL</b>. If <b>NULL</b>, discovery is modified on all local radios; if any radio is modified by the call, the function call succeeds.

### -param fEnabled

Flag specifying whether discovery is to be enabled or disabled. Set to <b>TRUE</b> to enable discovery, set to <b>FALSE</b> to disable discovery.

## -returns

Returns <b>TRUE</b> if the discovery state was successfully changed. If <i>hRadio</i> is <b>NULL</b>, a return value of <b>TRUE</b> indicates that at least one local radio state was successfully changed. Returns <b>FALSE</b> if discovery state was not changed; if <i>hRadio</i> was <b>NULL</b>, no radio accepted the state change.

## -remarks

Use the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisdiscoverable">BluetoothIsDiscoverable</a> function  to determine the current state of a Bluetooth radio.
Windows ensures that a discoverable system is connectable, and as such, the radio must allow incoming connections prior to making a radio 
discoverable. Failure to allow incoming connections results in the <b>BluetoothEnableDiscovery</b> function call failing.

When <b>BluetoothEnableDiscovery</b> changes the discovery state, the new state is valid for the lifetime of the calling application. Additionally, if a Bluetooth radio previously made discoverable with this function is disabled and re-enabled via the application, discoverability will not persist. Once the calling application terminates, the discovery  state of the specified Bluetooth radio reverts to the state it was in before <b>BluetoothEnableDiscovery</b> was called.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatedevice">BluetoothAuthenticateDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothauthenticatemultipledevices">BluetoothAuthenticateMultipleDevices</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothenableincomingconnections">BluetoothEnableIncomingConnections</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisconnectable">BluetoothIsConnectable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothisdiscoverable">BluetoothIsDiscoverable</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothregisterforauthentication">BluetoothRegisterForAuthentication</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsendauthenticationresponse">BluetoothSendAuthenticationResponse</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothunregisterauthentication">BluetoothUnregisterAuthentication</a>