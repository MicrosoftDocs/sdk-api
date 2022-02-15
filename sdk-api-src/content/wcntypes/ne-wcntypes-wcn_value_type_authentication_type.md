---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_AUTHENTICATION_TYPE
title: WCN_VALUE_TYPE_AUTHENTICATION_TYPE (wcntypes.h)
description: WCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration defines the authentication types supported by the Enrollee (access point or station).
helpviewer_keywords: ["WCN_VALUE_AT_OPEN","WCN_VALUE_AT_SHARED","WCN_VALUE_AT_WPA","WCN_VALUE_AT_WPA2","WCN_VALUE_AT_WPA2PSK","WCN_VALUE_AT_WPAPSK","WCN_VALUE_AT_WPAWPA2PSK_MIXED","WCN_VALUE_TYPE_AUTHENTICATION_TYPE","WCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration [Windows Connect Now]","wcn.wcn_value_type_authentication_type","wcntypes/WCN_VALUE_AT_OPEN","wcntypes/WCN_VALUE_AT_SHARED","wcntypes/WCN_VALUE_AT_WPA","wcntypes/WCN_VALUE_AT_WPA2","wcntypes/WCN_VALUE_AT_WPA2PSK","wcntypes/WCN_VALUE_AT_WPAPSK","wcntypes/WCN_VALUE_AT_WPAWPA2PSK_MIXED","wcntypes/WCN_VALUE_TYPE_AUTHENTICATION_TYPE"]
old-location: wcn\wcn_value_type_authentication_type.htm
tech.root: wcn
ms.assetid: fb69c89e-ab4b-4382-9bab-889552136da4
ms.date: 12/05/2018
ms.keywords: WCN_VALUE_AT_OPEN, WCN_VALUE_AT_SHARED, WCN_VALUE_AT_WPA, WCN_VALUE_AT_WPA2, WCN_VALUE_AT_WPA2PSK, WCN_VALUE_AT_WPAPSK, WCN_VALUE_AT_WPAWPA2PSK_MIXED, WCN_VALUE_TYPE_AUTHENTICATION_TYPE, WCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration [Windows Connect Now], wcn.wcn_value_type_authentication_type, wcntypes/WCN_VALUE_AT_OPEN, wcntypes/WCN_VALUE_AT_SHARED, wcntypes/WCN_VALUE_AT_WPA, wcntypes/WCN_VALUE_AT_WPA2, wcntypes/WCN_VALUE_AT_WPA2PSK, wcntypes/WCN_VALUE_AT_WPAPSK, wcntypes/WCN_VALUE_AT_WPAWPA2PSK_MIXED, wcntypes/WCN_VALUE_TYPE_AUTHENTICATION_TYPE
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
targetos: Windows
req.typenames: WCN_VALUE_TYPE_AUTHENTICATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_VALUE_TYPE_AUTHENTICATION_TYPE
 - wcntypes/tagWCN_VALUE_TYPE_AUTHENTICATION_TYPE
 - WCN_VALUE_TYPE_AUTHENTICATION_TYPE
 - wcntypes/WCN_VALUE_TYPE_AUTHENTICATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wcntypes.h
api_name:
 - WCN_VALUE_TYPE_AUTHENTICATION_TYPE
---

# WCN_VALUE_TYPE_AUTHENTICATION_TYPE enumeration


## -description

The <b>WCN_VALUE_TYPE_AUTHENTICATION_TYPE</b> enumeration defines the authentication  types supported by the Enrollee (access point or station).

## -enum-fields

### -field WCN_VALUE_AT_OPEN:0x1

Specifies IEEE 802.11 Open System authentication.

### -field WCN_VALUE_AT_WPAPSK:0x2

Specifies WPA security. Authentication is performed between the supplicant and authenticator over IEEE 802.1X. Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator. 

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_AT_SHARED:0x4

Specifies IEEE 802.11 Shared Key authentication that uses a preshared WEP key. 

<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_AT_WPA:0x8

Specifies WPA security. Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X. Encryption keys are dynamic and are derived through the authentication process. 

<div class="alert"><b>Note</b>  Not supported by most access points, consider WPA2PSK authentication instead.</div>
<div> </div>
<div class="alert"><b>Note</b>  Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_AT_WPA2:0x10

Specifies WPA2 security. Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X. Encryption keys are dynamic and are derived through the authentication process.

<div class="alert"><b>Note</b>  Not supported by most access points, consider WPA2PSK authentication instead.</div>
<div> </div>

### -field WCN_VALUE_AT_WPA2PSK:0x20

Specifies WPA2 security. Authentication is performed between the supplicant and authenticator over IEEE 802 1X. Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.

### -field WCN_VALUE_AT_WPAWPA2PSK_MIXED:0x22

Specifies WPAPSK/WPA2PSK mixed-mode encryption.

<div class="alert"><b>Note</b>  Available starting in Windows 8.1.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wcntypes/ne-wcntypes-wcn_attribute_type">WCN_ATTRIBUTE_TYPE</a>
