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

# ITsSbProvider::CreateEnvironmentPropertySetObject


## -description


Creates an <a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a> environment property set object.


## -parameters




### -param ppPropertySet [out]

A pointer to the created <a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a> environment property set object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins can use this method to create an environment property set object.




## -see-also




<a href="https://msdn.microsoft.com/613c972d-ab52-495a-a8fd-2827e39e9a4e">ITsSbEnvironmentPropertySet</a>



<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>
 

 

