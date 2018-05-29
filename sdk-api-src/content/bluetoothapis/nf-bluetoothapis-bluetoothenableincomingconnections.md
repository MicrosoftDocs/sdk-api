---
UID: NF:bluetoothapis.BluetoothEnableIncomingConnections
title: BluetoothEnableIncomingConnections function
author: windows-sdk-content
description: The BluetoothEnableIncomingConnections function modifies whether a local Bluetooth radio accepts incoming connections.
old-location: bluetooth\bluetoothenableincomingconnections.htm
old-project: Bluetooth
ms.assetid: 8f9c133e-e647-45c8-b2c6-372b18345637
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BluetoothEnableIncomingConnections, BluetoothEnableIncomingConnections function [Bluetooth], bluetooth.bluetoothenableincomingconnections, bluetoothapis/BluetoothEnableIncomingConnections
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bthprops.dll
-	BluetoothAPIs.dll
-	Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
-	BluetoothEnableIncomingConnections
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
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




<a href="https://msdn.microsoft.com/9f8ff768-a794-4a61-a215-ae17e9acf620">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/e20ad938-cab4-4017-95bf-8d6843f048eb">BluetoothIsConnectable</a>



<a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/4483f04e-09a2-4bd4-879c-c3a263c685de">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

