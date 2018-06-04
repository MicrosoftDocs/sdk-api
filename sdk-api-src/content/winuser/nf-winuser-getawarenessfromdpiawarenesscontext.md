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

# GetAwarenessFromDpiAwarenessContext function


## -description


Retrieves the <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a> value from a <b>DPI_AWARENESS_CONTEXT</b>.


## -parameters




### -param value [in]

The <b>DPI_AWARENESS_CONTEXT</b> you want to examine.


## -returns



The <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>. If the provided <i>value</i> is <b>null</b> or invalid, this method will return <b>DPI_AWARENESS_INVALID</b>.




## -remarks



A <a href="https://msdn.microsoft.com/BFD54A9F-642B-4A3A-BBB9-F3A80779251D">DPI_AWARENESS_CONTEXT</a> contains multiple pieces of information. For example, it includes both the current and the inherited <a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>. This method retrieves the <b>DPI_AWARENESS</b> from the structure.




## -see-also




<a href="https://msdn.microsoft.com/0E7EB331-7D72-4853-8785-03F30263C323">DPI_AWARENESS</a>
 

 

