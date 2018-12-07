---
UID: NF:clfsw32.AlignReservedLog
title: AlignReservedLog function
author: windows-sdk-content
description: Calculates the sector-aligned reservation size for a set of reserved records.
old-location: fs\alignreservedlog.htm
tech.root: Clfs
ms.assetid: 1ac8ecc7-a937-40cb-8a8b-8b168d9fce61
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AlignReservedLog, AlignReservedLog function [Files], clfsw32/AlignReservedLog, fs.alignreservedlog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - AlignReservedLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

