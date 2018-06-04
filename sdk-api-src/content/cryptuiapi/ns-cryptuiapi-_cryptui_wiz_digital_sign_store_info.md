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

# _CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO structure


## -description


<p class="CCE_Message">[The  <b>CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO</b> structure contains information about the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> used by the digital signature wizard.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure. This value must be set to <code>sizeof(CRYPTUI_WIZ_DIGITAL_SIGN_STORE_INFO)</code>.


### -field cCertStore

Number of certificates in the <b>rghCertStore</b> member.


### -field rghCertStore

A pointer to a handle to the certificate store that will be used by the digital signature wizard.


### -field pFilterCallback

Filter callback function used to display the certificate.


### -field pvCallbackData

A pointer to the callback data.

