---
UID: NS:bluetoothapis._BLUETOOTH_AUTHENTICATE_RESPONSE
title: "_BLUETOOTH_AUTHENTICATE_RESPONSE"
author: windows-sdk-content
description: BLUETOOTH_AUTHENTICATE_RESPONSE structure contains information passed in response to a BTH_REMOTE_AUTHENTICATE_REQUEST event.
old-location: bluetooth\bluetooth_authenticate_response.htm
tech.root: bluetooth
ms.assetid: fc7eda84-3e7b-49e9-a1a6-e1759c894e1a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PBLUETOOTH_AUTHENTICATE_RESPONSE, BLUETOOTH_AUTHENTICATE_RESPONSE, BLUETOOTH_AUTHENTICATE_RESPONSE structure [Bluetooth], PBLUETOOTH_AUTHENTICATE_RESPONSE, PBLUETOOTH_AUTHENTICATE_RESPONSE structure pointer [Bluetooth], _BLUETOOTH_AUTHENTICATE_RESPONSE, bluetooth.bluetooth_authenticate_response, bluetoothapis/BLUETOOTH_AUTHENTICATE_RESPONSE, bluetoothapis/PBLUETOOTH_AUTHENTICATE_RESPONSE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_AUTHENTICATE_RESPONSE
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_AUTHENTICATE_RESPONSE, *PBLUETOOTH_AUTHENTICATE_RESPONSE
req.redist: 
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
 

 

