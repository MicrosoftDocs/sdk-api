---
UID: NF:bluetoothapis.BluetoothFindRadioClose
title: BluetoothFindRadioClose function
author: windows-sdk-content
description: The BluetoothFindRadioClose function closes the enumeration handle associated with finding Bluetooth radios.
old-location: bluetooth\bluetoothfindradioclose.htm
tech.root: bluetooth
ms.assetid: 859771b1-d06c-414b-81cb-bb3913fd0380
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: BluetoothFindRadioClose, BluetoothFindRadioClose function [Bluetooth], bluetooth.bluetoothfindradioclose, bluetoothapis/BluetoothFindRadioClose
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
 - BluetoothFindRadioClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothFindRadioClose function


## -description


The <b>BluetoothFindRadioClose</b> function closes the enumeration handle associated with finding Bluetooth radios.


## -parameters




### -param hFind

Enumeration handle to close, obtained with a previous call to the <a href="https://msdn.microsoft.com/en-us/library/Aa362786(v=VS.85).aspx">BluetoothFindFirstRadio</a> function.


## -returns



Returns <b>TRUE</b> when the handle is successfully closed. Returns <b>FALSE</b> if the attempt fails to close the enumeration handle. For additional information on possible errors associated with closing the handle, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362926(v=VS.85).aspx">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362786(v=VS.85).aspx">BluetoothFindFirstRadio</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362790(v=VS.85).aspx">BluetoothFindNextRadio</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362797(v=VS.85).aspx">BluetoothGetRadioInfo</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

