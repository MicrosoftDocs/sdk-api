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

# MFCreateContentProtectionDevice function


## -description


Creates an <a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a> interface for the specified media protection system.


## -parameters




### -param ProtectionSystemId [in]

The idenfier of the media protection system for which you want to create the <a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a> interface.


### -param ContentProtectionDevice [out]

Pointer to the created <a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

