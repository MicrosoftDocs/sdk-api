---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_CONFIG_METHODS
title: WCN_VALUE_TYPE_CONFIG_METHODS (wcntypes.h)
description: WCN_VALUE_TYPE_CONFIG_METHODS enumeration defines the configuration methods supported by the Enrollee or Registrar.
helpviewer_keywords: ["WCN_VALUE_CM_DISPLAY","WCN_VALUE_CM_ETHERNET","WCN_VALUE_CM_EXTERNAL_NFC","WCN_VALUE_CM_INTEGRATED_NFC","WCN_VALUE_CM_KEYPAD","WCN_VALUE_CM_LABEL","WCN_VALUE_CM_NFC_INTERFACE","WCN_VALUE_CM_PHYS_DISPLAY","WCN_VALUE_CM_PHYS_PUSHBUTTON","WCN_VALUE_CM_PUSHBUTTON","WCN_VALUE_CM_USBA","WCN_VALUE_CM_VIRT_DISPLAY","WCN_VALUE_CM_VIRT_PUSHBUTTON","WCN_VALUE_TYPE_CONFIG_METHODS","WCN_VALUE_TYPE_CONFIG_METHODS enumeration [Windows Connect Now]","wcn.wcn_value_type_config_methods","wcntypes/WCN_VALUE_CM_DISPLAY","wcntypes/WCN_VALUE_CM_ETHERNET","wcntypes/WCN_VALUE_CM_EXTERNAL_NFC","wcntypes/WCN_VALUE_CM_INTEGRATED_NFC","wcntypes/WCN_VALUE_CM_KEYPAD","wcntypes/WCN_VALUE_CM_LABEL","wcntypes/WCN_VALUE_CM_NFC_INTERFACE","wcntypes/WCN_VALUE_CM_PHYS_DISPLAY","wcntypes/WCN_VALUE_CM_PHYS_PUSHBUTTON","wcntypes/WCN_VALUE_CM_PUSHBUTTON","wcntypes/WCN_VALUE_CM_USBA","wcntypes/WCN_VALUE_CM_VIRT_DISPLAY","wcntypes/WCN_VALUE_CM_VIRT_PUSHBUTTON","wcntypes/WCN_VALUE_TYPE_CONFIG_METHODS"]
old-location: wcn\wcn_value_type_config_methods.htm
tech.root: wcn
ms.assetid: 7fa4ff2a-4ba2-43ac-9ebc-5baf04e802bc
ms.date: 12/05/2018
ms.keywords: WCN_VALUE_CM_DISPLAY, WCN_VALUE_CM_ETHERNET, WCN_VALUE_CM_EXTERNAL_NFC, WCN_VALUE_CM_INTEGRATED_NFC, WCN_VALUE_CM_KEYPAD, WCN_VALUE_CM_LABEL, WCN_VALUE_CM_NFC_INTERFACE, WCN_VALUE_CM_PHYS_DISPLAY, WCN_VALUE_CM_PHYS_PUSHBUTTON, WCN_VALUE_CM_PUSHBUTTON, WCN_VALUE_CM_USBA, WCN_VALUE_CM_VIRT_DISPLAY, WCN_VALUE_CM_VIRT_PUSHBUTTON, WCN_VALUE_TYPE_CONFIG_METHODS, WCN_VALUE_TYPE_CONFIG_METHODS enumeration [Windows Connect Now], wcn.wcn_value_type_config_methods, wcntypes/WCN_VALUE_CM_DISPLAY, wcntypes/WCN_VALUE_CM_ETHERNET, wcntypes/WCN_VALUE_CM_EXTERNAL_NFC, wcntypes/WCN_VALUE_CM_INTEGRATED_NFC, wcntypes/WCN_VALUE_CM_KEYPAD, wcntypes/WCN_VALUE_CM_LABEL, wcntypes/WCN_VALUE_CM_NFC_INTERFACE, wcntypes/WCN_VALUE_CM_PHYS_DISPLAY, wcntypes/WCN_VALUE_CM_PHYS_PUSHBUTTON, wcntypes/WCN_VALUE_CM_PUSHBUTTON, wcntypes/WCN_VALUE_CM_USBA, wcntypes/WCN_VALUE_CM_VIRT_DISPLAY, wcntypes/WCN_VALUE_CM_VIRT_PUSHBUTTON, wcntypes/WCN_VALUE_TYPE_CONFIG_METHODS
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
req.typenames: WCN_VALUE_TYPE_CONFIG_METHODS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_VALUE_TYPE_CONFIG_METHODS
 - wcntypes/tagWCN_VALUE_TYPE_CONFIG_METHODS
 - WCN_VALUE_TYPE_CONFIG_METHODS
 - wcntypes/WCN_VALUE_TYPE_CONFIG_METHODS
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
 - WCN_VALUE_TYPE_CONFIG_METHODS
---

# WCN_VALUE_TYPE_CONFIG_METHODS enumeration


## -description

The <b>WCN_VALUE_TYPE_CONFIG_METHODS</b> enumeration defines the configuration methods supported by the Enrollee or Registrar. One or more of the following configuration methods must be supported.

## -enum-fields

### -field WCN_VALUE_CM_USBA:0x1

USB-A (flash drive) configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7 and later. Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CM_ETHERNET:0x2

Ethernet configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7 and later. Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CM_LABEL:0x4

Label configuration is supported. To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

### -field WCN_VALUE_CM_DISPLAY:0x8

Display configuration is supported. To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  For WPS 2.0, use <b>WCN_VALUE_CM_VIRT_DISPLAY</b> or <b>WCN_VALUE_CM_PHYS_DISPLAY</b>.</div>
<div> </div>

### -field WCN_VALUE_CM_EXTERNAL_NFC:0x10

External near-field communication (NFC) token configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_INTEGRATED_NFC:0x20

Integrated NFC token configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_NFC_INTERFACE:0x40

NFC interface configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_PUSHBUTTON:0x80

Push button configuration is supported. To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  For WPS 2.0, use <b>WCN_VALUE_CM_VIRT_PUSHBUTTON</b> or <b>WCN_VALUE_CM_PHYS_PUSHBUTTON</b>.</div>
<div> </div>

### -field WCN_VALUE_CM_KEYPAD:0x100

Keypad configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_VIRT_PUSHBUTTON:0x280

Virtual push button configuration is supported.  To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_VALUE_CM_PHYS_PUSHBUTTON:0x480

Physical push button configuration is supported.  To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_VALUE_CM_VIRT_DISPLAY:0x2008

Virtual display configuration is supported. To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_VALUE_CM_PHYS_DISPLAY:0x4008

Physical display configuration is supported. To authenticate with the default password ID, call <a href="/windows/desktop/api/wcndevice/nf-wcndevice-iwcndevice-setpassword">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="/windows/desktop/api/wcndevice/ne-wcndevice-wcn_password_type">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wcntypes/ne-wcntypes-wcn_attribute_type">WCN_ATTRIBUTE_TYPE</a>
