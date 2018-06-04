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

# BCRYPT_INIT_AUTH_MODE_INFO macro


## -description


The <b>BCRYPT_INIT_AUTH_MODE_INFO</b> macro  initializes a <a href="https://msdn.microsoft.com/6c00f458-7198-44fe-bdb6-2c2eb9995bd9">BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO</a> structure for use in calls to <a href="https://msdn.microsoft.com/69fe4530-4b7c-40db-a85c-f9dc458735e7">BCryptEncrypt</a> and <a href="https://msdn.microsoft.com/62286f6b-0d57-4691-83fc-2b9a9740af71">BCryptDecrypt</a> functions.


## -parameters




### -param _AUTH_INFO_STRUCT_

The BCRYPT_AUTHENTICATED_CIPHER_MODE_INFO structure to initialize.

