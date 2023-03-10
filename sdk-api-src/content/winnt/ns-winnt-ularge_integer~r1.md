---
UID: NS:winnt._ULARGE_INTEGER~r1
title: ULARGE_INTEGER
description: The ULARGE_INTEGER structure represents a 64-bit unsigned integer value. (ULARGE_INTEGER union (winnt.h))
ms.date: 08/03/2022
ms.keywords: _ULARGE_INTEGER, ULARGE_INTEGER
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: ULARGE_INTEGER
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _ULARGE_INTEGER
 - winnt/_ULARGE_INTEGER
 - ULARGE_INTEGER
 - winnt/ULARGE_INTEGER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winnt.h
api_name:
 - _ULARGE_INTEGER
 - ULARGE_INTEGER
---

# ULARGE_INTEGER structure


## -description

Represents a 64-bit unsigned integer value.
<div class="alert"><b>Note</b>  Your C compiler may support 64-bit integers natively. For example, Microsoft Visual C++ supports the <a href="/windows/desktop/Midl/--int64">__int64</a> sized integer type. For more information, see the documentation included with your C compiler.</div><div> </div>

## -struct-fields

### -field DUMMYSTRUCTNAME

### -field LowPart

The low-order 32 bits.

### -field HighPart

The high-order 32 bits.

### -field u

### -field QuadPart

An unsigned 64-bit integer.

## -remarks

The <b>ULARGE_INTEGER</b> structure is actually a union. If your compiler has built-in support for 64-bit integers, use the <b>QuadPart</b> member to store the 64-bit integer. Otherwise, use the <b>LowPart</b> and <b>HighPart</b> members to store the 64-bit integer.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>

<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>
