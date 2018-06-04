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

# tagWCN_VALUE_TYPE_CONFIG_METHODS enumeration


## -description


The <b>WCN_VALUE_TYPE_CONFIG_METHODS</b> enumeration defines the configuration methods supported by the Enrollee or Registrar. One or more of the following configuration methods must be supported.


## -enum-fields




### -field WCN_VALUE_CM_USBA

USB-A (flash drive) configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7 and later. Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CM_ETHERNET

Ethernet configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7 and later. Not supported in WPS 2.0.</div>
<div> </div>

### -field WCN_VALUE_CM_LABEL

Label configuration is supported. To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.


### -field WCN_VALUE_CM_DISPLAY

Display configuration is supported. To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  For WPS 2.0, use <b>WCN_VALUE_CM_VIRT_DISPLAY</b> or <b>WCN_VALUE_CM_PHYS_DISPLAY</b>.</div>
<div> </div>

### -field WCN_VALUE_CM_EXTERNAL_NFC

External near-field communication (NFC) token configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_INTEGRATED_NFC

Integrated NFC token configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_NFC_INTERFACE

NFC interface configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_PUSHBUTTON

Push button configuration is supported. To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  For WPS 2.0, use <b>WCN_VALUE_CM_VIRT_PUSHBUTTON</b> or <b>WCN_VALUE_CM_PHYS_PUSHBUTTON</b>.</div>
<div> </div>

### -field WCN_VALUE_CM_KEYPAD

Keypad configuration is supported.

<div class="alert"><b>Note</b>  Not supported in Windows 7.</div>
<div> </div>

### -field WCN_VALUE_CM_VIRT_PUSHBUTTON

Virtual push button configuration is supported.  To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_VALUE_CM_PHYS_PUSHBUTTON

Physical push button configuration is supported.  To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the push button password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_VALUE_CM_VIRT_DISPLAY

Virtual display configuration is supported. To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_VALUE_CM_PHYS_DISPLAY

Physical display configuration is supported. To authenticate with the default password ID, call <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a> with the PIN password type defined by <a href="https://msdn.microsoft.com/14bdc3d4-11eb-4361-bd28-3399c14c4d08">WCN_PASSWORD_TYPE</a>.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

