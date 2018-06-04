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

# AllocReservedLog function


## -description


Allocates sector-aligned space  for a set of reserved records.  The requested allocation must  be  the  same size   that <a href="https://msdn.microsoft.com/1ac8ecc7-a937-40cb-8a8b-8b168d9fce61">AlignReservedLog</a> returns.


## -parameters




### -param pvMarshal [in, out]

A pointer to the  marshaling context that is allocated by calling the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param cReservedRecords [in]

The number of reserved records that are associated with the reservation adjustment.  

This value must be greater than zero (0).


### -param pcbAdjustment [in, out]

The size of the sector-aligned space reservation that is associated with the number of records specified in <i>cReservedRecords</i>, in bytes.  

This parameter must be the aligned reservation size  that  <a href="https://msdn.microsoft.com/1ac8ecc7-a937-40cb-8a8b-8b168d9fce61">AlignReservedLog</a> returns in <i>*pcbAlignReservation</i>. 


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the possible  error codes:




## -see-also




<a href="https://msdn.microsoft.com/1ac8ecc7-a937-40cb-8a8b-8b168d9fce61">AlignReservedLog</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

