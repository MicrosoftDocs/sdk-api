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

# _CROSS_CERT_DIST_POINTS_INFO structure


## -description


The <b>CROSS_CERT_DIST_POINTS_INFO</b> structure provides information used to update dynamic cross certificates.


## -struct-fields




### -field dwSyncDeltaTime

<b>DWORD</b> indicating seconds between synchronization. If this member is zero, the client default synchronization time is used.


### -field cDistPoint

Count of the number of elements in the <b>rgDistPoint</b> member array.


### -field rgDistPoint

Array of 
<a href="https://msdn.microsoft.com/f9a20827-3333-4ce2-b074-2e8ce903fad2">CERT_ALT_NAME_INFO</a> structures for distribution points for updating cross certificates.

