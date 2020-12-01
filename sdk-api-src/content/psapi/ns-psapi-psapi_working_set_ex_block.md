---
UID: NS:psapi._PSAPI_WORKING_SET_EX_BLOCK
title: PSAPI_WORKING_SET_EX_BLOCK (psapi.h)
description: Contains extended working set information for a page.
helpviewer_keywords: ["*PPSAPI_WORKING_SET_EX_BLOCK","PPSAPI_WORKING_SET_EX_BLOCK","PPSAPI_WORKING_SET_EX_BLOCK union pointer [PSAPI]","PSAPI_WORKING_SET_EX_BLOCK","PSAPI_WORKING_SET_EX_BLOCK union [PSAPI]","base.psapi_working_set_ex_block","psapi.psapi_working_set_ex_block","psapi/PPSAPI_WORKING_SET_EX_BLOCK","psapi/PSAPI_WORKING_SET_EX_BLOCK"]
old-location: psapi\psapi_working_set_ex_block.htm
tech.root: psapi
ms.assetid: 4ba17fa0-2aed-4099-9380-fc13f1b826ca
ms.date: 12/05/2018
ms.keywords: '*PPSAPI_WORKING_SET_EX_BLOCK, PPSAPI_WORKING_SET_EX_BLOCK, PPSAPI_WORKING_SET_EX_BLOCK union pointer [PSAPI], PSAPI_WORKING_SET_EX_BLOCK, PSAPI_WORKING_SET_EX_BLOCK union [PSAPI], base.psapi_working_set_ex_block, psapi.psapi_working_set_ex_block, psapi/PPSAPI_WORKING_SET_EX_BLOCK, psapi/PSAPI_WORKING_SET_EX_BLOCK'
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: PSAPI_WORKING_SET_EX_BLOCK, *PPSAPI_WORKING_SET_EX_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PSAPI_WORKING_SET_EX_BLOCK
 - psapi/_PSAPI_WORKING_SET_EX_BLOCK
 - PPSAPI_WORKING_SET_EX_BLOCK
 - psapi/PPSAPI_WORKING_SET_EX_BLOCK
 - PSAPI_WORKING_SET_EX_BLOCK
 - psapi/PSAPI_WORKING_SET_EX_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - PSAPI_WORKING_SET_EX_BLOCK
---

# PSAPI_WORKING_SET_EX_BLOCK structure


## -description

Contains extended working set information for a page.

## -struct-fields

### -field Flags

The working set information. See the description of the structure  members for information about the layout 
      of this variable.

### -field Valid

If this bit is 1, the subsequent members are valid; otherwise they should be ignored.

### -field ShareCount

The number of processes that share this page. The maximum value of this member is 7.

### -field Win32Protection

The memory protection attributes of the page. For a list of values, see
       <a href="/windows/desktop/Memory/memory-protection-constants">Memory Protection Constants</a>.

### -field Shared

If this bit is 1, the page can be shared.

### -field Node

The NUMA node. The maximum value of this member is 63.

### -field Locked

If this bit is 1, the virtual page is locked in physical memory.

### -field LargePage

If this bit is 1, the page is a large page.

### -field Reserved

Reserved.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available before Windows Server 2012 and Windows 8.

### -field Bad

If this bit is 1, the page is has been reported as bad.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available before Windows Server 2012 and Windows 8.

### -field ReservedUlong

Reserved. This member is only available on 64-bit code running on 64-bit editions of Windows.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available before Windows Server 2012 and Windows 8.

### -field Invalid

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This structure is not available before Windows Server 2012 and Windows 8.

### -field Invalid.Valid

If this bit is 0, the subsequent members are valid; otherwise they should be ignored.

### -field Invalid.Reserved0

Reserved.

### -field Invalid.Shared

If this bit is 1, the page can be shared.

### -field Invalid.Reserved1

Reserved.

### -field Invalid.Bad

If this bit is 1, the page is has been reported as bad.

### -field Invalid.ReservedUlong

Reserved. This member is only available on 64-bit code running on 64-bit editions of Windows.

## -see-also

<a href="/windows/desktop/psapi/psapi-structures">PSAPI Structures</a>



<a href="/windows/desktop/api/psapi/ns-psapi-psapi_working_set_ex_information">PSAPI_WORKING_SET_EX_INFORMATION</a>



<a href="/windows/desktop/api/psapi/nf-psapi-queryworkingsetex">QueryWorkingSetEx</a>