---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_CONFIGURATION_ERROR
title: WCN_VALUE_TYPE_CONFIGURATION_ERROR
author: windows-sdk-content
description: WCN_VALUE_TYPE_CONFIGURATION_ERROR enumeration defines possible error values returned to a device while attempting to configure to, and associate with, the WLAN.
old-location: wcn\wcn_value_type_configuration_error.htm
tech.root: wcn
ms.assetid: 52653dd0-d563-4a3d-a461-d38ea0e327a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WCN_VALUE_CE_2_4_CHANNEL_NOT_SUPPORTED, WCN_VALUE_CE_5_0_CHANNEL_NOT_SUPPORTED, WCN_VALUE_CE_COULD_NOT_CONNECT_TO_REGISTRAR, WCN_VALUE_CE_DECRYPTION_CRC_FAILURE, WCN_VALUE_CE_DEVICE_BUSY, WCN_VALUE_CE_DEVICE_PASSWORD_AUTH_FAILURE, WCN_VALUE_CE_FAILED_DHCP_CONFIG, WCN_VALUE_CE_IP_ADDRESS_CONFLICT, WCN_VALUE_CE_MESSAGE_TIMEOUT, WCN_VALUE_CE_MULTIPLE_PBC_SESSIONS_DETECTED, WCN_VALUE_CE_NETWORK_ASSOCIATION_FAILURE, WCN_VALUE_CE_NETWORK_AUTHENTICATION_FAILURE, WCN_VALUE_CE_NO_DHCP_RESPONSE, WCN_VALUE_CE_NO_ERROR, WCN_VALUE_CE_OOB_INTERFACE_READ_ERROR, WCN_VALUE_CE_REGISTRATION_SESSION_TIMEOUT, WCN_VALUE_CE_ROGUE_ACTIVITY_SUSPECTED, WCN_VALUE_CE_SETUP_LOCKED, WCN_VALUE_CE_SIGNAL_TOO_WEAK, WCN_VALUE_TYPE_CONFIGURATION_ERROR, WCN_VALUE_TYPE_CONFIGURATION_ERROR enumeration [Windows Connect Now], wcn.wcn_value_type_configuration_error, wcntypes/WCN_VALUE_CE_2_4_CHANNEL_NOT_SUPPORTED, wcntypes/WCN_VALUE_CE_5_0_CHANNEL_NOT_SUPPORTED, wcntypes/WCN_VALUE_CE_COULD_NOT_CONNECT_TO_REGISTRAR, wcntypes/WCN_VALUE_CE_DECRYPTION_CRC_FAILURE, wcntypes/WCN_VALUE_CE_DEVICE_BUSY, wcntypes/WCN_VALUE_CE_DEVICE_PASSWORD_AUTH_FAILURE, wcntypes/WCN_VALUE_CE_FAILED_DHCP_CONFIG, wcntypes/WCN_VALUE_CE_IP_ADDRESS_CONFLICT, wcntypes/WCN_VALUE_CE_MESSAGE_TIMEOUT, wcntypes/WCN_VALUE_CE_MULTIPLE_PBC_SESSIONS_DETECTED, wcntypes/WCN_VALUE_CE_NETWORK_ASSOCIATION_FAILURE, wcntypes/WCN_VALUE_CE_NETWORK_AUTHENTICATION_FAILURE, wcntypes/WCN_VALUE_CE_NO_DHCP_RESPONSE, wcntypes/WCN_VALUE_CE_NO_ERROR, wcntypes/WCN_VALUE_CE_OOB_INTERFACE_READ_ERROR, wcntypes/WCN_VALUE_CE_REGISTRATION_SESSION_TIMEOUT, wcntypes/WCN_VALUE_CE_ROGUE_ACTIVITY_SUSPECTED, wcntypes/WCN_VALUE_CE_SETUP_LOCKED, wcntypes/WCN_VALUE_CE_SIGNAL_TOO_WEAK, wcntypes/WCN_VALUE_TYPE_CONFIGURATION_ERROR
ms.topic: enum
req.header: wcntypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - wcntypes.h
api_name:
 - WCN_VALUE_TYPE_CONFIGURATION_ERROR
product: Windows
targetos: Windows
req.typenames: WCN_VALUE_TYPE_CONFIGURATION_ERROR
req.redist: 
---

# WCN_VALUE_TYPE_CONFIGURATION_ERROR enumeration


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
 

 

