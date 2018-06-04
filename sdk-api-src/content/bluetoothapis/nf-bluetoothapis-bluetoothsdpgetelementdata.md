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

# BluetoothSdpGetElementData function


## -description


The <b>BluetoothSdpGetElementData</b> function retrieves and parses a single element from an SDP stream.


## -parameters




### -param pSdpStream [in]

A pointer to a valid SDP stream.


### -param cbSdpStreamLength

TBD


### -param pData [out]

A pointer to a buffer to be filled with the data of the SDP element found at the beginning of the <i>pSdpStream</i> SDP stream.


#### - cbSpdStreamLength [in]

The length, in bytes, of <i>pSdpStream</i>.


## -returns



Returns <b>ERROR_SUCCESS</b> when the SDP element is parsed correctly. Returns <b>ERROR_INVALID_PARAMETER</b> if one of the required parameters is <b>NULL</b>, or if the SDP stream pointed to by <i>pSdpStream</i> is not valid.




## -see-also




<a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/7dbf44f6-8a80-419e-9db7-60ada9ca9647">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/26a68fe3-6ffb-44ff-b9db-757d35022a41">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/16ff7951-08a7-49c5-93a5-0782cca50dab">SDP_STRING_TYPE_DATA</a>
 

 

