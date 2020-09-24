---
UID: NF:clfsw32.AllocReservedLog
title: AllocReservedLog function (clfsw32.h)
description: Allocates sector-aligned space for a set of reserved records.
helpviewer_keywords: ["AllocReservedLog","AllocReservedLog function [Files]","clfsw32/AllocReservedLog","fs.allocreservedlog"]
old-location: fs\allocreservedlog.htm
tech.root: fs
ms.assetid: 5e464b64-4617-4fbd-97cd-3c2db8f151b2
ms.date: 12/05/2018
ms.keywords: AllocReservedLog, AllocReservedLog function [Files], clfsw32/AllocReservedLog, fs.allocreservedlog
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AllocReservedLog
 - clfsw32/AllocReservedLog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - AllocReservedLog
---

# AllocReservedLog function


## -description

Allocates sector-aligned space  for a set of reserved records.  The requested allocation must  be  the  same size   that <a href="/windows/desktop/api/clfsw32/nf-clfsw32-alignreservedlog">AlignReservedLog</a> returns.

## -parameters

### -param pvMarshal [in, out]

A pointer to the  marshaling context that is allocated by calling the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

### -param cReservedRecords [in]

The number of reserved records that are associated with the reservation adjustment.  

This value must be greater than zero (0).

### -param pcbAdjustment [in, out]

The size of the sector-aligned space reservation that is associated with the number of records specified in <i>cReservedRecords</i>, in bytes.  

This parameter must be the aligned reservation size  that  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-alignreservedlog">AlignReservedLog</a> returns in <i>*pcbAlignReservation</i>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following  list identifies the possible  error codes:

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-alignreservedlog">AlignReservedLog</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>