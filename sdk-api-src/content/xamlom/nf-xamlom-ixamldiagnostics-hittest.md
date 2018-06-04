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

# IXamlDiagnostics::HitTest


## -description


Gets all elements in the visual tree that fall within the specified rectangle.


## -parameters




### -param rect [in]

The area to hit test.


### -param pCount [out]

The size of the array.


### -param ppInstanceHandles [out]

An array containing all elements.


## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method performs a hit test on the XAML visual tree and will return all elements
    regardless if they are enabled or invisible for hit testing. This method does not return collapsed elements as they do not participate in layout. <a href="https://msdn.microsoft.com/83971154-4E40-474C-91AD-2436B1D02CB8">AdviseVisualTreeChange</a>
    must be called before this method. The element does not need to be fully enclosed in the 
    <i>rect</i> area to be returned.




## -see-also




<a href="https://msdn.microsoft.com/1BCE3EC3-8B48-4F16-8E91-78776C07F309">IXamlDiagnostics</a>
 

 

