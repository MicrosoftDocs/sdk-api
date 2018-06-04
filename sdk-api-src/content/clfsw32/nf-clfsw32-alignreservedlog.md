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

# AlignReservedLog function


## -description


Calculates the sector-aligned reservation size for a set of reserved records.  This value is then passed to <a href="https://msdn.microsoft.com/5e464b64-4617-4fbd-97cd-3c2db8f151b2">AllocReservedLog</a> to reserve a block of log space for a set of records.


## -parameters




### -param pvMarshal [in, out]

A pointer to the opaque marshaling context that is allocated by calling the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param cReservedRecords [in]

The number of reserved records that are associated with the reservation adjustment.


### -param rgcbReservation [in]

An array of space allocations  to reserve in the log that is associated with the current marshaling context, in bytes.  

The number of allocations corresponds to the number of records  that  <i>cReservedRecords</i> specifies.  Each allocation must be greater than zero (0) or  the function fails with <b>ERROR_INVALID_PARAMETER</b>.


### -param pcbAlignReservation [out]

A pointer to a variable in which the function returns the number of   sector-aligned byte space to be reserved in the log—after being given the number of records  that  <i>cRecords</i> specifies and the size of reservations specified in the <i>rgcbReservation</i> array.

  The value returned in <i>*pcbAlignReservation</i> is used as input to <a href="https://msdn.microsoft.com/5e464b64-4617-4fbd-97cd-3c2db8f151b2">AllocReservedLog</a>. If  <b>AllocReservedLog</b> succeeds, this value is always greater than zero (0).  If <b>AllocReservedLog</b> fails, the value is zero (0).


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/5e464b64-4617-4fbd-97cd-3c2db8f151b2">AllocReservedLog</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>
 

 

