---
UID: NS:winnt._ULARGE_INTEGER~r1
title: ULARGE_INTEGER
ms.date: 01/30/19
ms.keywords: _ULARGE_INTEGER, ULARGE_INTEGER
ms.topic: language-reference
targetos: Windows
product: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winnt.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: ULARGE_INTEGER
req.umdf-ver: 
req.unicode-ansi: 
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
<div class="alert"><b>Note</b>  Your C compiler may support 64-bit integers natively. For example, Microsoft Visual C++ supports the <a href="https://msdn.microsoft.com/52fafae2-003c-4eae-b6e1-a49f69db204e">__int64</a> sized integer type. For more information, see the documentation included with your C compiler.</div><div> </div>


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

<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>

<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>

<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
