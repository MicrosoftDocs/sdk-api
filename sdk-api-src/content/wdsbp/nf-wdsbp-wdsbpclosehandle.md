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

# WdsBpCloseHandle function


## -description


Closes the specified handle.


## -parameters




### -param hHandle [in]

A handle to be closed. This can be a handle obtained using the <a href="https://msdn.microsoft.com/dc6007ad-0dd5-477d-a49f-45820aa1b5f6">WdsBpParseInitialize</a> or <a href="https://msdn.microsoft.com/a77cbdf5-9025-4e98-8edd-1b9bae8493e7">WdsBpInitialize</a> functions.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



