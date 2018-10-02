---
UID: NC:bluetoothapis.PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK
title: PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK
author: windows-sdk-content
description: A callback function prototype that is called once for each attribute found in the pSDPStream parameter passed to the BluetoothSdpEnumAttributes function call.
old-location: bluetooth\pfn_bluetooth_enum_attributes_callback.htm
tech.root: Bluetooth
ms.assetid: 4d728467-1866-428f-9e66-a45b597a226a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK, PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK callback, PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK callback function [Bluetooth], bluetooth.pfn_bluetooth_enum_attributes_callback, bluetoothapis/PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - BluetoothAPIs.h
api_name:
 - PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK callback function


## -description


The <i>PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</i> is a callback function prototype that is called once for each attribute found in the <b>pSDPStream</b> parameter passed to the <a href="https://msdn.microsoft.com/en-us/library/Aa362885(v=VS.85).aspx">BluetoothSdpEnumAttributes</a> function call.


## -parameters




### -param uAttribId

The current attribute identifier in the SDP stream.


### -param pValueStream

The raw SDP stream for the attribute value associated with <b>uAttribId</b>. Use the <a href="https://msdn.microsoft.com/en-us/library/Aa362889(v=VS.85).aspx">BluetoothSdpGetElementData</a> function to parse the raw results into computer-readable data.


### -param cbStreamSize

The size, in bytes, of <b>pValueStream</b>.


### -param pvParam

The context passed in from a previous call to the <a href="https://msdn.microsoft.com/en-us/library/Aa362885(v=VS.85).aspx">BluetoothSdpEnumAttributes</a> function.


## -returns



Should return <b>TRUE</b> when the enumeration continues to the next attribute identifier found in the stream. Should return <b>FALSE</b> when  enumeration of the record attribute identifiers should immediately stop.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362889(v=VS.85).aspx">BluetoothSdpGetElementData</a>
 

 

