---
UID: NF:bluetoothapis.BluetoothSdpGetElementData
title: BluetoothSdpGetElementData function (bluetoothapis.h)
author: windows-sdk-content
description: Retrieves and parses a single element from an SDP stream.
old-location: bluetooth\bluetoothsdpgetelementdata.htm
tech.root: bluetooth
ms.assetid: 65de8f2f-1781-44fa-87a9-21aa461eb8ee
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BluetoothSdpGetElementData, BluetoothSdpGetElementData function [Bluetooth], bluetooth.bluetoothsdpgetelementdata, bluetoothapis/BluetoothSdpGetElementData
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
 - BluetoothSdpGetElementData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/7dbf44f6-8a80-419e-9db7-60ada9ca9647">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/26a68fe3-6ffb-44ff-b9db-757d35022a41">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/16ff7951-08a7-49c5-93a5-0782cca50dab">SDP_STRING_TYPE_DATA</a>
 

 

