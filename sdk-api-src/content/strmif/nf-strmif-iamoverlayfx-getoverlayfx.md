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

# IAMOverlayFX::GetOverlayFX


## -description



The <code>GetOverlayFX</code> method retrieves the effects currently applied to the overlay surface, if any. The application can call this method while the filter graph is running.




## -parameters




### -param lpdwOverlayFX [out]

Pointer a variable that receives a value indicating which effects, if any, are currently applied to the overlay surface. The value is a logical combination of flags from the <a href="https://msdn.microsoft.com/fa984504-5175-4b94-8a75-d294cd9546a4">AMOVERLAYFX</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_POINTER to indicate a <b>NULL</b> pointer argument.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6bc78464-8c9e-4016-b9aa-6589d53d45bf">IAMOverlayFX Interface</a>
 

 

