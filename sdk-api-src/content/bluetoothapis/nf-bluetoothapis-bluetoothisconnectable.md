---
UID: NF:bluetoothapis.BluetoothIsConnectable
title: BluetoothIsConnectable function
author: windows-sdk-content
description: The BluetoothIsConnectable function determines whether a Bluetooth radio or radios is connectable.
old-location: bluetooth\bluetoothisconnectable.htm
old-project: Bluetooth
ms.assetid: e20ad938-cab4-4017-95bf-8d6843f048eb
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: BluetoothIsConnectable, BluetoothIsConnectable function [Bluetooth], bluetooth.bluetoothisconnectable, bluetoothapis/BluetoothIsConnectable
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
tech.root: 
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
-	BluetoothIsConnectable
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothIsConnectable function


## -description


The <b>BluetoothIsConnectable</b> function determines whether a Bluetooth radio or radios is connectable.


## -parameters




### -param hRadio

Valid local radio handle, or <b>NULL</b>. If <b>NULL</b>, all local radios are checked for connectability; if any radio is connectable, the function call succeeds.


## -returns



Returns <b>TRUE</b> if at least one Bluetooth radio is accepting incoming connections. Returns <b>FALSE</b> if no radios are accepting incoming connections.




## -remarks



If multiple Bluetooth radios exist, the first radio to return that it is connectable causes the <b>BluetoothIsConnectable</b> function to succeed.




## -see-also




<a href="https://msdn.microsoft.com/9f8ff768-a794-4a61-a215-ae17e9acf620">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/8f9c133e-e647-45c8-b2c6-372b18345637">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/33d34e36-dc17-4029-91bd-53ece5a93b4b">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/f85dd076-9062-413f-863f-9d3baba322ad">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/4483f04e-09a2-4bd4-879c-c3a263c685de">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/bfb1a18c-e5b1-4053-8652-5a76b196bebe">BluetoothUnregisterAuthentication</a>
 

 

