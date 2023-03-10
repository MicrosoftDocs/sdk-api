---
UID: NS:ntdef._LUID
title: LUID (ntdef.h)
description: The LUID structure is an opaque structure that specifies an identifier that is guaranteed to be unique on the local machine. For more information, see the reference page for LUID in the Microsoft Windows SDK documentation.
helpviewer_keywords: ["*PLUID","LUID","LUID structure [Kernel-Mode Driver Architecture]","PLUID","PLUID structure pointer [Kernel-Mode Driver Architecture]","kernel.luid","kstruct_c_0aa22a8e-19fe-40b3-96b1-9aed87ac58c3.xml","ntdef/PLUID","ntdef/SINGLE_LIST_ENTRY"]
old-location: kernel\luid.htm
tech.root: Kernel
ms.assetid: 974536eb-5cb3-4056-9c43-c6df170f6bf7
ms.date: 12/05/2018
ms.keywords: '*PLUID, LUID, LUID structure [Kernel-Mode Driver Architecture], PLUID, PLUID structure pointer [Kernel-Mode Driver Architecture], kernel.luid, kstruct_c_0aa22a8e-19fe-40b3-96b1-9aed87ac58c3.xml, ntdef/PLUID, ntdef/SINGLE_LIST_ENTRY'
req.header: ntdef.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LUID, *PLUID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LUID
 - ntdef/_LUID
 - PLUID
 - ntdef/PLUID
 - LUID
 - ntdef/LUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdef.h
api_name:
 - LUID
---

# LUID structure


## -description

The <b>LUID</b> structure is an opaque structure that specifies an identifier that is guaranteed to be unique on the local machine. For more information, see the reference page for <b>LUID</b> in the Microsoft Windows SDK documentation.

## -struct-fields

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-rtlconvertlongtoluid">RtlConvertLongToLuid</a>



<a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-rtlconvertulongtoluid">RtlConvertUlongToLuid</a>



<a href="/windows-hardware/drivers/kernel/mm-bad-pointer">RtlEqualLuid</a>



<a href="/windows-hardware/drivers/kernel/mm-bad-pointer">RtlIsZeroLuid</a>