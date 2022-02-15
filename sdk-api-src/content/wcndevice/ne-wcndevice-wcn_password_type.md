---
UID: NE:wcndevice.tagWCN_PASSWORD_TYPE
title: WCN_PASSWORD_TYPE (wcndevice.h)
description: WCN_PASSWORD_TYPE enumeration defines the authentication that will be used in a WPS session.
helpviewer_keywords: ["WCN_PASSWORD_TYPE","WCN_PASSWORD_TYPE enumeration [Windows Connect Now]","WCN_PASSWORD_TYPE_PIN","WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED","WCN_PASSWORD_TYPE_PUSH_BUTTON","wcn.wcn_password_type","wcndevice/WCN_PASSWORD_TYPE","wcndevice/WCN_PASSWORD_TYPE_PIN","wcndevice/WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED","wcndevice/WCN_PASSWORD_TYPE_PUSH_BUTTON"]
old-location: wcn\wcn_password_type.htm
tech.root: wcn
ms.assetid: 14bdc3d4-11eb-4361-bd28-3399c14c4d08
ms.date: 12/05/2018
ms.keywords: WCN_PASSWORD_TYPE, WCN_PASSWORD_TYPE enumeration [Windows Connect Now], WCN_PASSWORD_TYPE_PIN, WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED, WCN_PASSWORD_TYPE_PUSH_BUTTON, wcn.wcn_password_type, wcndevice/WCN_PASSWORD_TYPE, wcndevice/WCN_PASSWORD_TYPE_PIN, wcndevice/WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED, wcndevice/WCN_PASSWORD_TYPE_PUSH_BUTTON
req.header: wcndevice.h
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
req.typenames: WCN_PASSWORD_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_PASSWORD_TYPE
 - wcndevice/tagWCN_PASSWORD_TYPE
 - WCN_PASSWORD_TYPE
 - wcndevice/WCN_PASSWORD_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wcndevice.h
api_name:
 - WCN_PASSWORD_TYPE
---

# WCN_PASSWORD_TYPE enumeration


## -description

The <b>WCN_PASSWORD_TYPE</b> enumeration defines the authentication that will be used in a WPS session.

## -enum-fields

### -field WCN_PASSWORD_TYPE_PUSH_BUTTON:0

Indicates the device uses a WPS button interface to put the device into wireless provisioning mode. If this value is specified when calling <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a>, set <i>dwPasswordLength</i> to zero and <i>pbPassword</i> to <b>NULL</b>.

### -field WCN_PASSWORD_TYPE_PIN

Indicates that authentication is secured via a PIN. The user must provide the PIN of the device. Usually, the PIN is a 4 or 8-digit number printed on a label attached to the device, or displayed on the screen. If this value is specified when calling <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a>, set <i>dwPasswordLength</i> to the number of digits in the password, and <i>pbPassword</i> to point to a buffer containing the ASCII representation of the pin.

### -field WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED

Indicates that authentication is secured via a PIN, as above, but that the PIN is specified by the registrar.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_PASSWORD_TYPE_OOB_SPECIFIED

### -field WCN_PASSWORD_TYPE_WFDS

## -see-also

<a href="/windows/desktop/api/wcntypes/ne-wcntypes-wcn_attribute_type">WCN_ATTRIBUTE_TYPE</a>
