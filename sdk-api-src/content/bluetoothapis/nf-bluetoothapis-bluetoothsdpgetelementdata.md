---
UID: NF:bluetoothapis.BluetoothSdpGetElementData
title: BluetoothSdpGetElementData function
author: windows-sdk-content
description: Retrieves and parses a single element from an SDP stream.
old-location: bluetooth\bluetoothsdpgetelementdata.htm
old-project: bluetooth
ms.assetid: 65de8f2f-1781-44fa-87a9-21aa461eb8ee
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BluetoothSdpGetElementData, BluetoothSdpGetElementData function [Bluetooth], bluetooth.bluetoothsdpgetelementdata, bluetoothapis/BluetoothSdpGetElementData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothSdpGetElementData
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothSdpGetElementData function


## -description


The <b>BluetoothSdpGetElementData</b> function retrieves and parses a single element from an SDP stream.


## -parameters




### -param pSdpStream [in]

A pointer to a valid SDP stream.


### -param cbSdpStreamLength [in]

The length, in bytes, of <i>pSdpStream</i>.


### -param pData [out]

A pointer to a buffer to be filled with the data of the SDP element found at the beginning of the <i>pSdpStream</i> SDP stream.


## -returns



Returns <b>ERROR_SUCCESS</b> when the SDP element is parsed correctly. Returns <b>ERROR_INVALID_PARAMETER</b> if one of the required parameters is <b>NULL</b>, or if the SDP stream pointed to by <i>pSdpStream</i> is not valid.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362885(v=VS.85).aspx">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362887(v=VS.85).aspx">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362890(v=VS.85).aspx">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363054(v=VS.85).aspx">SDP_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363055(v=VS.85).aspx">SDP_STRING_TYPE_DATA</a>
 

 

