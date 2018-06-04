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

# Pack2UINT32AsUINT64 function


## -description


Packs two <b>UINT32</b> values into a <b>UINT64</b> value.


## -parameters




### -param unHigh [in]

Value to store in the high-order 32 bits of the <b>UINT64</b> value.


### -param unLow [in]

Value to store in the low-order 32 bits of the <b>UINT64</b> value.


## -returns



Returns the packed <b>UINT64</b> value.




## -remarks



This function stores two 32-bit values in a 64-bit value that is suitable for the <a href="https://msdn.microsoft.com/817ed1c1-16ad-4520-a1a0-a93563936b50">IMFAttributes::SetUINT64</a> method.




## -see-also




<a href="https://msdn.microsoft.com/04e8c89e-115e-41d4-b8cb-953f68ddd14e">MFSetAttributeRatio</a>



<a href="https://msdn.microsoft.com/cf7b3cfe-fdce-417d-8c0b-198d026b8768">MFSetAttributeSize</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

