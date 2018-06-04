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

# IXpsOMVisual::SetHyperlinkNavigateUri


## -description


Sets the destination URI of the visual's hyperlink.


## -parameters




### -param hyperlinkUri [in]

The <a href="http://go.microsoft.com/fwlink/p/?linkid=116163">IUri</a> interface that contains the destination URI of the visual's hyperlink.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Setting an object's URI makes the object a hyperlink. When activated or clicked, the object   will navigate to the destination that is  specified by the URI in <i>hyperlinkUri</i>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=116163">IUri</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

