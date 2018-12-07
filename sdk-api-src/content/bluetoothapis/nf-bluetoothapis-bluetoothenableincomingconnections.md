---
UID: NF:bluetoothapis.BluetoothEnableIncomingConnections
title: BluetoothEnableIncomingConnections function
author: windows-sdk-content
description: The BluetoothEnableIncomingConnections function modifies whether a local Bluetooth radio accepts incoming connections.
old-location: bluetooth\bluetoothenableincomingconnections.htm
tech.root: Bluetooth
ms.assetid: 8f9c133e-e647-45c8-b2c6-372b18345637
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BluetoothEnableIncomingConnections, BluetoothEnableIncomingConnections function [Bluetooth], bluetooth.bluetoothenableincomingconnections, bluetoothapis/BluetoothEnableIncomingConnections
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
 - BluetoothEnableIncomingConnections
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothEnableIncomingConnections function


## -description


The <b>BluetoothEnableIncomingConnections</b> function modifies whether a local Bluetooth radio accepts incoming connections.


## -parameters




### -param hRadio

Valid local radio handle for which to change whether incoming connections are enabled, or <b>NULL</b>. If <b>NULL</b>, the attempt to modify incoming connection acceptance iterates through all local radios; if any radio is modified by the call, the function call succeeds.


### -param fEnabled

Flag specifying whether incoming connection acceptance is to be enabled or disabled. Set to <b>TRUE</b> to enable incoming connections, set to <b>FALSE</b> to disable incoming connections.


## -returns



Returns <b>TRUE</b> if the incoming connection  state was successfully changed. If <i>hRadio</i> is <b>NULL</b>, a return value of <b>TRUE</b> indicates that at least one local radio state was successfully changed. Returns <b>FALSE</b> if incoming connection  state was not changed; if <i>hRadio</i> was <b>NULL</b>, no radio accepted the state change.




## -remarks



 A  radio that is non-connectable is non-discoverable. The radio must be made non-discoverable  prior to making a radio non-connectable. Failure to make a radio non-discoverable prior to making it non-connectable will result in failure of the <b>BluetoothEnableIncomingConnections</b> function call.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362770(v=VS.85).aspx">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362776(v=VS.85).aspx">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362799(v=VS.85).aspx">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362893(v=VS.85).aspx">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a>
 

 

