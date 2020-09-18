---
UID: NF:lmapibuf.NetApiBufferReallocate
title: NetApiBufferReallocate function (lmapibuf.h)
description: The NetApiBufferReallocate function changes the size of a buffer allocated by a previous call to the NetApiBufferAllocate function.
helpviewer_keywords: ["NetApiBufferReallocate","NetApiBufferReallocate function [Network Management]","_win32_netapibufferreallocate","lmapibuf/NetApiBufferReallocate","netmgmt.netapibufferreallocate"]
old-location: netmgmt\netapibufferreallocate.htm
tech.root: NetMgmt
ms.assetid: 61153de0-33d3-4c83-a8aa-a7179252328c
ms.date: 12/05/2018
ms.keywords: NetApiBufferReallocate, NetApiBufferReallocate function [Network Management], _win32_netapibufferreallocate, lmapibuf/NetApiBufferReallocate, netmgmt.netapibufferreallocate
req.header: lmapibuf.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetApiBufferReallocate
 - lmapibuf/NetApiBufferReallocate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetApiBufferReallocate
---

# NetApiBufferReallocate function


## -description

The 
				<b>NetApiBufferReallocate</b> function changes the size of a buffer allocated by a previous call to the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function.

## -parameters

### -param OldBuffer [in]

Pointer to the buffer returned by a call to the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function.

### -param NewByteCount [in]

Specifies the new size of the buffer, in bytes.

### -param NewBuffer [out]

Receives the pointer to the reallocated buffer.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required to successfully execute the ApiBuffer functions.

For a code sample that demonstrates how to use the network management 
<a href="/windows/desktop/NetMgmt/apibuffer-functions">ApiBuffer functions</a>, see 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a>.

## -see-also

<a href="/windows/desktop/NetMgmt/apibuffer-functions">Api Buffer
		  Functions</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>