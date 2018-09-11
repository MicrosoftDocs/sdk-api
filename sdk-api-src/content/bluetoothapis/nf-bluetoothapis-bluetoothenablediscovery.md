---
UID: NF:bluetoothapis.BluetoothEnableDiscovery
title: BluetoothEnableDiscovery function
author: windows-sdk-content
description: The BluetoothEnableDiscovery function changes the discovery state of a local Bluetooth radio or radios.
old-location: bluetooth\bluetoothenablediscovery.htm
tech.root: bluetooth
ms.assetid: ca28c9cd-a271-48fa-901c-e99e063854d5
ms.author: windowssdkdev
ms.date: 08/06/2018
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



Use the <a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a> function  to determine the current state of a Bluetooth radio.
Windows ensures that a discoverable system is connectable, and as such, the radio must allow incoming connections prior to making a radio 
discoverable. Failure to allow incoming connections results in the <b>BluetoothEnableDiscovery</b> function call failing.

When <b>BluetoothEnableDiscovery</b> changes the discovery state, the new state is valid for the lifetime of the calling application. Additionally, if a Bluetooth radio previously made discoverable with this function is disabled and re-enabled via the application, discoverability will not persist. Once the calling application terminates, the discovery  state of the specified Bluetooth radio reverts to the state it was in before <b>BluetoothEnableDiscovery</b> was called.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362770(v=VS.85).aspx">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362778(v=VS.85).aspx">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362799(v=VS.85).aspx">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362893(v=VS.85).aspx">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a>
 

 

