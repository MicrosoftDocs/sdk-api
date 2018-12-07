---
UID: NF:bluetoothapis.BluetoothIsConnectable
title: BluetoothIsConnectable function
author: windows-sdk-content
description: The BluetoothIsConnectable function determines whether a Bluetooth radio or radios is connectable.
old-location: bluetooth\bluetoothisconnectable.htm
tech.root: Bluetooth
ms.assetid: e20ad938-cab4-4017-95bf-8d6843f048eb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BluetoothIsConnectable, BluetoothIsConnectable function [Bluetooth], bluetooth.bluetoothisconnectable, bluetoothapis/BluetoothIsConnectable
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
 - BluetoothIsConnectable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/en-us/library/Aa362770(v=VS.85).aspx">BluetoothAuthenticateDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362772(v=VS.85).aspx">BluetoothAuthenticateMultipleDevices</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362776(v=VS.85).aspx">BluetoothEnableDiscovery</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362778(v=VS.85).aspx">BluetoothEnableIncomingConnections</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362882(v=VS.85).aspx">BluetoothIsDiscoverable</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362883(v=VS.85).aspx">BluetoothRegisterForAuthentication</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362893(v=VS.85).aspx">BluetoothSendAuthenticationResponse</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362895(v=VS.85).aspx">BluetoothUnregisterAuthentication</a>
 

 

