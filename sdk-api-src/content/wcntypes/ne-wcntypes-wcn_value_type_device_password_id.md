---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_DEVICE_PASSWORD_ID
title: WCN_VALUE_TYPE_DEVICE_PASSWORD_ID (wcntypes.h)
description: WCN_VALUE_TYPE_DEVICE_PASSWORD_ID enumeration defines values that specify the origin or 'type' of a password.
helpviewer_keywords: ["WCN_VALUE_DP_DEFAULT","WCN_VALUE_DP_MACHINE_SPECIFIED","WCN_VALUE_DP_PUSHBUTTON","WCN_VALUE_DP_REGISTRAR_SPECIFIED","WCN_VALUE_DP_REKEY","WCN_VALUE_DP_USER_SPECIFIED","WCN_VALUE_TYPE_DEVICE_PASSWORD_ID","WCN_VALUE_TYPE_DEVICE_PASSWORD_ID enumeration [Windows Connect Now]","wcn.wcn_value_type_device_password_id","wcntypes/WCN_VALUE_DP_DEFAULT","wcntypes/WCN_VALUE_DP_MACHINE_SPECIFIED","wcntypes/WCN_VALUE_DP_PUSHBUTTON","wcntypes/WCN_VALUE_DP_REGISTRAR_SPECIFIED","wcntypes/WCN_VALUE_DP_REKEY","wcntypes/WCN_VALUE_DP_USER_SPECIFIED","wcntypes/WCN_VALUE_TYPE_DEVICE_PASSWORD_ID"]
old-location: wcn\wcn_value_type_device_password_id.htm
tech.root: wcn
ms.assetid: 3642bb5d-ef19-4ff3-a8bc-b0f01ad197ce
ms.date: 12/05/2018
ms.keywords: WCN_VALUE_DP_DEFAULT, WCN_VALUE_DP_MACHINE_SPECIFIED, WCN_VALUE_DP_PUSHBUTTON, WCN_VALUE_DP_REGISTRAR_SPECIFIED, WCN_VALUE_DP_REKEY, WCN_VALUE_DP_USER_SPECIFIED, WCN_VALUE_TYPE_DEVICE_PASSWORD_ID, WCN_VALUE_TYPE_DEVICE_PASSWORD_ID enumeration [Windows Connect Now], wcn.wcn_value_type_device_password_id, wcntypes/WCN_VALUE_DP_DEFAULT, wcntypes/WCN_VALUE_DP_MACHINE_SPECIFIED, wcntypes/WCN_VALUE_DP_PUSHBUTTON, wcntypes/WCN_VALUE_DP_REGISTRAR_SPECIFIED, wcntypes/WCN_VALUE_DP_REKEY, wcntypes/WCN_VALUE_DP_USER_SPECIFIED, wcntypes/WCN_VALUE_TYPE_DEVICE_PASSWORD_ID
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
req.typenames: WCN_VALUE_TYPE_DEVICE_PASSWORD_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_VALUE_TYPE_DEVICE_PASSWORD_ID
 - wcntypes/tagWCN_VALUE_TYPE_DEVICE_PASSWORD_ID
 - WCN_VALUE_TYPE_DEVICE_PASSWORD_ID
 - wcntypes/WCN_VALUE_TYPE_DEVICE_PASSWORD_ID
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
 - WCN_VALUE_TYPE_DEVICE_PASSWORD_ID
---

# WCN_VALUE_TYPE_DEVICE_PASSWORD_ID enumeration


## -description

The <b>WCN_VALUE_TYPE_DEVICE_PASSWORD_ID</b> enumeration defines values that specify the origin or 'type' of a password.

## -enum-fields

### -field WCN_VALUE_DP_DEFAULT:0

The PIN password, obtained from the label, or
display will be used. This password may correspond to the label, display, or a user-defined password that has been
configured to replace the original device password.


To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

### -field WCN_VALUE_DP_USER_SPECIFIED:0x1

The user has overridden the default password with a manually selected value.


<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_DP_MACHINE_SPECIFIED:0x2

The default PIN password has been overridden by a strong, machine-generated
device password value. 

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_DP_REKEY:0x3

The 256-bit rekeying password
associated with the device will be used.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_DP_PUSHBUTTON:0x4

A password entered via a push button interface will be used. 

To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

### -field WCN_VALUE_DP_REGISTRAR_SPECIFIED:0x5

A PIN has been obtained from the Registrar via a display or
other out-of-band method. 

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_DP_NFC_CONNECTION_HANDOVER:0x7

### -field WCN_VALUE_DP_WFD_SERVICES:0x8

### -field WCN_VALUE_DP_OUTOFBAND_MIN:0x10

### -field WCN_VALUE_DP_OUTOFBAND_MAX:0xffff

## -see-also

<a href="/windows/desktop/api/wcntypes/ne-wcntypes-wcn_attribute_type">WCN_ATTRIBUTE_TYPE</a>
