---
UID: NE:wcndevice.tagWCN_PASSWORD_TYPE
title: tagWCN_PASSWORD_TYPE
author: windows-sdk-content
description: WCN_PASSWORD_TYPE enumeration defines the authentication that will be used in a WPS session.
old-location: wcn\wcn_password_type.htm
old-project: wcn
ms.assetid: 14bdc3d4-11eb-4361-bd28-3399c14c4d08
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: WCN_PASSWORD_TYPE, WCN_PASSWORD_TYPE enumeration [Windows Connect Now], WCN_PASSWORD_TYPE_PIN, WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED, WCN_PASSWORD_TYPE_PUSH_BUTTON, tagWCN_PASSWORD_TYPE, wcn.wcn_password_type, wcndevice/WCN_PASSWORD_TYPE, wcndevice/WCN_PASSWORD_TYPE_PIN, wcndevice/WCN_PASSWORD_TYPE_PIN_REGISTRAR_SPECIFIED, wcndevice/WCN_PASSWORD_TYPE_PUSH_BUTTON
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WCN_PASSWORD_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wcndevice.h
api_name:
-	WCN_PASSWORD_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

