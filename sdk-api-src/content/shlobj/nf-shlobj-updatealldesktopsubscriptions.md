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

# UpdateAllDesktopSubscriptions function


## -description


Deprecated. Enumerates the URLs of all the Desktop components and then tests to see if they are subscribed to. If they are subscribed to, the subscriptions are delivered.


## -parameters






#### - padp2

Type: <b><a href="https://msdn.microsoft.com/f67cc6c0-183c-4da2-9648-68a86dccfd78">IADesktopP2</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/f67cc6c0-183c-4da2-9648-68a86dccfd78">IADesktopP2</a> interface.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if components are subscribed to; otherwise <b>FALSE</b>.



