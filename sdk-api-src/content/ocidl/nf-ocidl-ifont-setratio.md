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

# IFont::SetRatio


## -description


Converts the scaling factor for this font between logical units and <b>HIMETRIC</b> units. 
    <b>HIMETRIC</b> units are used to express the point size in the 
    <a href="https://msdn.microsoft.com/aeee7dfc-5ccd-4c30-a59e-5eec93505288">IFont::get_Size</a> and 
    <a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">IFont::put_Size</a> methods. The values passed to 
    <b>IFont::SetRatio</b> are used to compute the display size of 
    the font in logical units from the value in the <b>Size</b> property:

<code>Display Size = ( cyLogical / cyHimetric ) * Size</code>


## -parameters




### -param cyLogical [in]

The font size, in logical units.


### -param cyHimetric [in]

The font size, in <b>HIMETRIC</b> units.


## -returns



The method supports the standard return values E_UNEXPECTED, E_INVALIDARG, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/3a04d2b7-b2eb-4c6c-8863-1e88321fa382">IFont</a>



<a href="https://msdn.microsoft.com/aeee7dfc-5ccd-4c30-a59e-5eec93505288">IFont::get_Size</a>



<a href="https://msdn.microsoft.com/1c39a7dc-553b-41b7-8b66-1a5980493dce">IFont::put_Size</a>
 

 

