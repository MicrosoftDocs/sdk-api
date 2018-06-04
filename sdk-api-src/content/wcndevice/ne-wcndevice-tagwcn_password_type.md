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

# tagWCN_PASSWORD_TYPE enumeration


## -description


The <b>WCN_PASSWORD_TYPE</b> enumeration defines the authentication that will be used in a WPS session.


## -enum-fields




### -field WCN_PASSWORD_TYPE_PUSH_BUTTON

Indicates the device uses a WPS button interface to put the device into wireless provisioning mode. If this value is specified when calling <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a>, set <i>dwPasswordLength</i> to zero and <i>pbPassword</i> to <b>NULL</b>.


### -field WCN_PASSWORD_TYPE_PIN

Indicates that authentication is secured via a PIN. The user must provide the PIN of the device. Usually, the PIN is a 4 or 8-digit number printed on a label attached to the device, or displayed on the screen. If this value is specified when calling <a href="https://msdn.microsoft.com/51d03336-3861-4585-b493-d6765c28b1eb">IWCNDevice::SetPassword</a>, set <i>dwPasswordLength</i> to the number of digits in the password, and <i>pbPassword</i> to point to a buffer containing the ASCII representation of the pin.


### -field WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED

Indicates that authentication is secured via a PIN, as above, but that the PIN is specified by the registrar.

<div class="alert"><b>Note</b>  Only available  in Windows 8.</div>
<div> </div>

### -field WCN_PASSWORD_TYPE_OOB_SPECIFIED


### -field WCN_PASSWORD_TYPE_WFDS




## -see-also




<a href="https://msdn.microsoft.com/214b64c3-b1f0-46b1-b52a-b1df1bb40cf7">WCN_ATTRIBUTE_TYPE</a>
 

 

