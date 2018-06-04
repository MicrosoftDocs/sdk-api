---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK callback function


## -description


The <i>PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</i> is a callback function prototype that is called once for each attribute found in the <b>pSDPStream</b> parameter passed to the <a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a> function call.


## -parameters




### -param uAttribId

The current attribute identifier in the SDP stream.


### -param pValueStream

The raw SDP stream for the attribute value associated with <b>uAttribId</b>. Use the <a href="https://msdn.microsoft.com/65de8f2f-1781-44fa-87a9-21aa461eb8ee">BluetoothSdpGetElementData</a> function to parse the raw results into computer-readable data.


### -param cbStreamSize

The size, in bytes, of <b>pValueStream</b>.


### -param pvParam

The context passed in from a previous call to the <a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a> function.


## -returns



Should return <b>TRUE</b> when the enumeration continues to the next attribute identifier found in the stream. Should return <b>FALSE</b> when  enumeration of the record attribute identifiers should immediately stop.




## -see-also




<a href="https://msdn.microsoft.com/65de8f2f-1781-44fa-87a9-21aa461eb8ee">BluetoothSdpGetElementData</a>
 

 

