---
UID: NF:winddi.EngProbeForRead
title: EngProbeForRead function (winddi.h)
description: The EngProbeForRead function probes a structure for read accessibility.
helpviewer_keywords: ["EngProbeForRead","EngProbeForRead function [Display Devices]","display.engprobeforread","gdifncs_35c5929d-d559-42ea-9925-b00bc7af551e.xml","winddi/EngProbeForRead"]
old-location: display\engprobeforread.htm
tech.root: display
ms.assetid: 7c64c9a8-45e6-4afa-a358-457c04a333d7
ms.date: 12/05/2018
ms.keywords: EngProbeForRead, EngProbeForRead function [Display Devices], display.engprobeforread, gdifncs_35c5929d-d559-42ea-9925-b00bc7af551e.xml, winddi/EngProbeForRead
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngProbeForRead
 - winddi/EngProbeForRead
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngProbeForRead
---

# EngProbeForRead function


## -description

The <b>EngProbeForRead</b> function probes a structure for read accessibility.

## -parameters

### -param Address [in]

Pointer to the structure to be probed.

### -param Length [in]

Specifies the length, in bytes, of the structure to be probed.

### -param Alignment [in]

Specifies the required alignment of the structure, expressed as the number of bytes in the base data type. For example, an alignment of 1 indicates that <i>Address</i> be aligned on a BYTE boundary, 2 specifies alignment on a WORD boundary, and 4 specifies alignment on a DWORD boundary.

## -returns

None

## -remarks

<b>EngProbeForRead</b> causes an exception to be raised if the structure pointed to by <i>Address</i>:

<ul>
<li>
Does not have a base address that begins on an <i>alignment</i>-byte boundary.

</li>
<li>
Is not read-accessible.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engprobeforreadandwrite">EngProbeForReadAndWrite</a>