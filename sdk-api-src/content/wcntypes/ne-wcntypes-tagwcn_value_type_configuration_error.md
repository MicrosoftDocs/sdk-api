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

# tagWCN_VALUE_TYPE_CONFIGURATION_ERROR enumeration


## -description


The <b>WCN_VALUE_TYPE_CONFIGURATION_ERROR</b> enumeration defines  possible error values returned to a device while attempting to configure to, and associate with, the WLAN.


## -enum-fields




### -field WCN_VALUE_CE_NO_ERROR

No error. An application must be prepared to handle devices that signal 'No Error' even if the device detected an error.


### -field WCN_VALUE_CE_OOB_INTERFACE_READ_ERROR

Could not read the out-of-band (OOB) interface.


### -field WCN_VALUE_CE_DECRYPTION_CRC_FAILURE

Could not decrypt the Cyclic Redundancy Check (CRC) value.


### -field WCN_VALUE_CE_2_4_CHANNEL_NOT_SUPPORTED

The 2.4 GHz channel is not supported.


### -field WCN_VALUE_CE_5_0_CHANNEL_NOT_SUPPORTED

The 5.0 GHz channel is not supported.


### -field WCN_VALUE_CE_SIGNAL_TOO_WEAK

The wireless signal is not strong enough to initiate a connection. 

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_NETWORK_AUTHENTICATION_FAILURE

Network authentication failed.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_NETWORK_ASSOCIATION_FAILURE

Network association failed.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_NO_DHCP_RESPONSE

The DHCP server did not respond.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_FAILED_DHCP_CONFIG

DHCP configuration failed.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_IP_ADDRESS_CONFLICT

There was an IP address conflict.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_COULD_NOT_CONNECT_TO_REGISTRAR

Could not connect to the registrar.


### -field WCN_VALUE_CE_MULTIPLE_PBC_SESSIONS_DETECTED

Multiple push button configuration (PBC) sessions were detected.


### -field WCN_VALUE_CE_ROGUE_ACTIVITY_SUSPECTED

Rogue activity is suspected.


### -field WCN_VALUE_CE_DEVICE_BUSY

The device is busy.


### -field WCN_VALUE_CE_SETUP_LOCKED

Setup is locked.


### -field WCN_VALUE_CE_MESSAGE_TIMEOUT

The message timed out.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_REGISTRATION_SESSION_TIMEOUT

The registration session timed out.

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CE_DEVICE_PASSWORD_AUTH_FAILURE

Device password authentication failed.


## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

