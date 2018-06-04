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

# tagWCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration


## -description


The <b>WCN_VALUE_TYPE_AUTHENTICATION_TYPE</b> enumeration defines the authentication  types supported by the Enrollee (access point or station).


## -enum-fields




### -field WCN_VALUE_AT_OPEN

Specifies IEEE 802.11 Open System authentication.


### -field WCN_VALUE_AT_WPAPSK

Specifies WPA security. Authentication is performed between the supplicant and authenticator over IEEE 802.1X. Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator. 

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_AT_SHARED

Specifies IEEE 802.11 Shared Key authentication that uses a preshared WEP key. 

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_AT_WPA

Specifies WPA security. Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X. Encryption keys are dynamic and are derived through the authentication process. 

<div class="alert"><b>Note</b>  Not supported by most access points, consider WPA2PSK authentication instead.</div>
<div> </div>
<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_AT_WPA2

Specifies WPA2 security. Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X. Encryption keys are dynamic and are derived through the authentication process.

<div class="alert"><b>Note</b>  Not supported by most access points, consider WPA2PSK authentication instead.</div>
<div> </div>

### -field WCN_VALUE_AT_WPA2PSK

Specifies WPA2 security. Authentication is performed between the supplicant and authenticator over IEEE 802 1X. Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.


### -field WCN_VALUE_AT_WPAWPA2PSK_MIXED

Specifies WPAPSK/WPA2PSK mixed-mode encryption.

<div class="alert"><b>Note</b>  Available starting in Windows 8.1.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

