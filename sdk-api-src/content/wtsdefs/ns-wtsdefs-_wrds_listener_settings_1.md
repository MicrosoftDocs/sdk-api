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

# _WRDS_LISTENER_SETTINGS_1 structure


## -description


Contains listener settings for a remote session.


## -struct-fields




### -field MaxProtocolListenerConnectionCount

The maximum number of protocol listener connections allowed. <b>ULONG_MAX</b> specifies the maximum number of connections.


### -field SecurityDescriptorSize.range

 


### -field SecurityDescriptorSize.range.0

 


### -field SecurityDescriptorSize.range.16384

 


### -field pSecurityDescriptor.size_is

 


### -field pSecurityDescriptor.size_is.SecurityDescriptorSize

 


### -field SecurityDescriptorSize

The size, in bytes, of the <b>pSecurityDescriptor</b> buffer.


### -field pSecurityDescriptor

The address of a buffer that contains the security descriptor for the protocol listener.

