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

# tagLHITTESTINFO structure


## -description


Used to get information about the link corresponding to a given location.



## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

Location for the hit-test, in client coordinates (not screen coordinates).



### -field item

Type: <b><a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a></b>

Receives information about the link corresponding to <b>pt</b>.


## -remarks



To convert from screen coordinates to client coordinates, use <a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a>.

<div class="alert"><b>Note</b>  If the <a href="https://msdn.microsoft.com/a84c0388-26e7-4eda-9c6c-c5f64142d67a">LM_HITTEST</a> message succeeds, the system fills in <a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM.iLink</a> and <b>LITEM.szID</b>. If the <b>LM_HITTEST</b> message fails, do not assume that any information in <b>LITEM</b> is valid.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a84c0388-26e7-4eda-9c6c-c5f64142d67a">LM_HITTEST</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a>
 

 

