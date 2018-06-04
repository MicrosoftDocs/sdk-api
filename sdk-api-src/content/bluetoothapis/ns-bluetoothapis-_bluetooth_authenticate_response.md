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

# _BLUETOOTH_AUTHENTICATE_RESPONSE structure


## -description


The <b>BLUETOOTH_AUTHENTICATE_RESPONSE</b> structure contains information passed in response to a BTH_REMOTE_AUTHENTICATE_REQUEST event.


## -struct-fields




### -field bthAddressRemote

A <a href="https://msdn.microsoft.com/2262a91b-c8b0-415a-9c23-7504998cc2a4">BLUETOOTH_ADDRESS</a> structure that contains the address of the device requesting the authentication response.  

<div class="alert"><b>Note</b>  This information can be found in the <a href="https://msdn.microsoft.com/e9c703c1-7981-4c34-a96e-0123d3655e55">PBLUETOOTH_AUTHENTICATION_CALLBACK PARAMS</a> structure retrieved from the callback.</div>
<div> </div>

### -field authMethod

A <a href="https://msdn.microsoft.com/2374df2c-2f50-4a06-aaad-384d81b067c5">BLUETOOTH_AUTHENTICATION_METHOD</a> enumeration that defines the supported authentication method. 

<div class="alert"><b>Note</b>  This information can be found in the <a href="https://msdn.microsoft.com/e9c703c1-7981-4c34-a96e-0123d3655e55">PBLUETOOTH_AUTHENTICATION_CALLBACK PARAMS</a> structure retrieved from the callback.</div>
<div> </div>

### -field pinInfo

 


### -field oobInfo

 


### -field numericCompInfo

 


### -field passkeyInfo

 


### -field negativeResponse

<b>TRUE</b> if the authentication request was rejected; otherwise <b>FALSE</b>.


#### - ( unnamed union )

 One of the following structures  must be used according to the authentication method defined in <i>authMethod</i>. For example, if  <b>BLUETOOTH_AUTHENTICATION_METHOD_LEGACY</b> is specified, the BLUETOOTH_PIN_INFO structure must be populated.  



#### pinInfo

Contains information for pin authentication.



#### oobInfo

Contains out-of-band data used to authenticate the device.



#### numericCompInfo

Contains information for numeric comparison authentication.



#### passkeyInfo

Contains information for passkey authentication.


## -see-also




<a href="https://msdn.microsoft.com/2374df2c-2f50-4a06-aaad-384d81b067c5">BLUETOOTH_AUTHENTICATION_METHOD</a>
 

 

