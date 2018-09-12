---
UID: NF:bluetoothapis.BluetoothFindDeviceClose
title: BluetoothFindDeviceClose function
author: windows-sdk-content
description: The BluetoothFindDeviceClose function closes an enumeration handle associated with a device query.
old-location: bluetooth\bluetoothfinddeviceclose.htm
tech.root: bluetooth
ms.assetid: 8b482d7f-56a3-47ef-be49-5272423c10f6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BluetoothFindDeviceClose, BluetoothFindDeviceClose function [Bluetooth], bluetooth.bluetoothfinddeviceclose, bluetoothapis/BluetoothFindDeviceClose
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
 - BluetoothFindDeviceClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BluetoothFindDeviceClose function


## -description


The <b>BluetoothFindDeviceClose</b> function closes an enumeration handle associated with a device query.


## -parameters




### -param hFind

Handle for the query to be closed. Obtained in a previous call to the <a href="https://msdn.microsoft.com/en-us/library/Aa362784(v=VS.85).aspx">BluetoothFindFirstDevice</a> function.


## -returns



Returns <b>TRUE</b> when the handle is successfully closed. Returns <b>FALSE</b> upon error. Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information on the failure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362924(v=VS.85).aspx">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362925(v=VS.85).aspx">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362774(v=VS.85).aspx">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362784(v=VS.85).aspx">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362788(v=VS.85).aspx">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362795(v=VS.85).aspx">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362884(v=VS.85).aspx">BluetoothRemoveDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362896(v=VS.85).aspx">BluetoothUpdateDeviceRecord</a>
 

 

