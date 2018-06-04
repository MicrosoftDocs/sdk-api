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

# translateurl_in_flags enumeration


## -description


The <b>TRANSLATEURL_IN_FLAGS</b> enumerated values are used with the <a href="https://msdn.microsoft.com/2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7">TranslateURL</a> function to determine how it will execute.


## -enum-fields




### -field TRANSLATEURL_FL_GUESS_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <a href="https://msdn.microsoft.com/2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7">TranslateURL</a>, the system automatically chooses a scheme and adds it to the URL.


### -field TRANSLATEURL_FL_USE_DEFAULT_PROTOCOL

If the protocol scheme is not specified in the <i>pcszURL</i> parameter to <a href="https://msdn.microsoft.com/2f089f5a-4d7c-4bb7-961c-5c6e3e73c7b7">TranslateURL</a>, the system adds the default protocol to the URL.

