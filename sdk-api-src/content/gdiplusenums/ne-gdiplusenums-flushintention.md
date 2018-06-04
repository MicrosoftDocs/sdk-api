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

# FlushIntention enumeration


## -description


The <b>FlushIntention</b> enumeration specifies when to flush the queue of graphics operations.


## -enum-fields




### -field FlushIntentionFlush

When passed to the 
				<a href="https://msdn.microsoft.com/76042de2-67d7-49b0-8a31-29fdc1a4e7be">Graphics::Flush</a> method, specifies that pending rendering operations are executed as soon as possible. The 
				<b>Graphics::Flush</b> method is not synchronized with the completion of the rendering operations and might return before the rendering operations are completed. 


### -field FlushIntentionSync

When passed to the 
				<a href="https://msdn.microsoft.com/76042de2-67d7-49b0-8a31-29fdc1a4e7be">Graphics::Flush</a> method, specifies that pending rendering operations are executed as soon as possible. The 
				<b>Graphics::Flush</b> method is synchronized with the completion of the rendering operations; that is, it will not return until after the rendering operations are completed. 

