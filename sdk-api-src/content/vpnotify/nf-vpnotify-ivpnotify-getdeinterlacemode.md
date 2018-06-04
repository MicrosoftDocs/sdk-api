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

# IVPNotify::GetDeinterlaceMode


## -description



The <code>GetDeinterlaceMode</code> method retrieves the mode (such as bob or weave).



This method is not currently implemented and returns E_NOTIMPL.


## -parameters




### -param pMode






#### - pmode [out]

Pointer to the retrieved mode. This value is a member of the <a href="https://msdn.microsoft.com/73d63ca2-17fb-4e27-9ea5-62686117254a">AMVP_MODE</a> enumerated data type.


## -returns



Returns E_NOTIMPL.




## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b40ba9e-8562-4d31-beaf-e4d4858bf145">IVPNotify Interface</a>
 

 

