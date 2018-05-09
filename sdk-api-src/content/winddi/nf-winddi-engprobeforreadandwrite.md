---
UID: NF:winddi.EngProbeForReadAndWrite
title: EngProbeForReadAndWrite function
author: windows-driver-content
description: The EngProbeForReadAndWrite function probes a structure for read and write accessibility.
old-location: display\engprobeforreadandwrite.htm
old-project: display
ms.assetid: 1b618bee-7069-410b-9a3d-65ee4b25874c
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: EngProbeForReadAndWrite, EngProbeForReadAndWrite function [Display Devices], display.engprobeforreadandwrite, gdifncs_a27f9e58-49c2-4c85-9f84-3aadc8776752.xml, winddi/EngProbeForReadAndWrite
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngProbeForReadAndWrite
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngProbeForReadAndWrite function


## -description


The <b>EngProbeForReadAndWrite</b> function probes a structure for read and write accessibility.


## -parameters




### -param Address [in, out]

Pointer to the structure to be probed.


### -param Length [in]

Specifies the length, in bytes, of the structure to be probed.


### -param Alignment [in]

Specifies the required alignment of the structure. This parameter is expressed as the number of bytes in the base data type. For example, an alignment of 1 indicates that <i>Address</i> be aligned on a BYTE boundary, 2 specifies alignment on a WORD boundary, and 4 specifies alignment on a DWORD boundary.


## -returns



None




## -remarks



<b>EngProbeForReadAndWrite</b> causes an exception to be raised if the structure pointed to by <i>Address</i>:

<ul>
<li>
Does not have a base address that begins on an <i>alignment</i>-byte boundary.

</li>
<li>
Is not both read- and write-accessible.

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564983">EngProbeForRead</a>
 

 

