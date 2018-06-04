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

# VisualMutationType enumeration


## -description


Defines constants that specify whether the element was added to or removed from the live visual tree.



## -enum-fields




### -field Add

The child element was added to the visual tree of the parent element.


### -field Remove

The child element was removed from the visual tree of the parent element.


## -remarks



<b>VisualMutationType</b> is used by <a href="https://msdn.microsoft.com/85B94DA2-11EF-49ED-8076-DA5AB36EF781">IVisualTreeServiceCallback</a> to indicate to the callback
whether the element is entering or leaving the live visual tree.



