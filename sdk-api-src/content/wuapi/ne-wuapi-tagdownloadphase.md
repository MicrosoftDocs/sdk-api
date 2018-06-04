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

# tagDownloadPhase enumeration


## -description


Defines the progress of the download of the current update that is returned by the <a href="https://msdn.microsoft.com/5c94b0e9-c137-4677-a014-b8467a8049e5">CurrentUpdateDownloadPhase</a> property of the <a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a> interface.


## -enum-fields




### -field dphInitializing

Initializing the download of the current update.


### -field dphDownloading

Downloading the current update.


### -field dphVerifying

Verifying the download of the current update.

