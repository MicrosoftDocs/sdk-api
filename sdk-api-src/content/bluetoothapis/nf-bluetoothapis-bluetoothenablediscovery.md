---
UID: NF:bluetoothapis.BluetoothEnableDiscovery
title: BluetoothEnableDiscovery function
author: windows-sdk-content
description: The BluetoothEnableDiscovery function changes the discovery state of a local Bluetooth radio or radios.
old-location: bluetooth\bluetoothenablediscovery.htm
tech.root: bluetooth
ms.assetid: ca28c9cd-a271-48fa-901c-e99e063854d5
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: BluetoothEnableDiscovery, BluetoothEnableDiscovery function [Bluetooth], bluetooth.bluetoothenablediscovery, bluetoothapis/BluetoothEnableDiscovery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.dll: Bthprops.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothEnableDiscovery
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



Use the <a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a> function  to determine the current state of a Bluetooth radio.
Windows ensures that a discoverable system is connectable, and as such, the radio must allow incoming connections prior to making a radio 
discoverable. Failure to allow incoming connections results in the <b>BluetoothEnableDiscovery</b> function call failing.

When <b>BluetoothEnableDiscovery</b> changes the discovery state, the new state is valid for the lifetime of the calling application. Additionally, if a Bluetooth radio previously made discoverable with this function is disabled and re-enabled via the application, discoverability will not persist. Once the calling application terminates, the discovery  state of the specified Bluetooth radio reverts to the state it was in before <b>BluetoothEnableDiscovery</b> was called.




## -see-also




<a href="https://msdn.microsoft.com/9f8ff768-a794-4a61-a215-ae17e9acf620">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/8f9c133e-e647-45c8-b2c6-372b18345637">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/e20ad938-cab4-4017-95bf-8d6843f048eb">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/4483f04e-09a2-4bd4-879c-c3a263c685de">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

