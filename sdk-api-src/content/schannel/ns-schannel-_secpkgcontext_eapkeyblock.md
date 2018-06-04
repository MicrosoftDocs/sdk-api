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

# _SecPkgContext_EapKeyBlock structure


## -description


The <b>SecPkgContext_EapKeyBlock</b> structure contains key data used by the EAP TLS Authentication Protocol. For information about the EAP TLS Authentication Protocol, see <a href="http://go.microsoft.com/fwlink/p/?linkid=84050">http://www.ietf.org/rfc/rfc2716.txt</a>.


## -struct-fields




### -field rgbKeys

An array of 128 bytes that contain key data used by the EAP TLS Authentication Protocol.


### -field rgbIVs

An array of 64 bytes that contain initialization vector data used by the EAP TLS Authentication Protocol.

