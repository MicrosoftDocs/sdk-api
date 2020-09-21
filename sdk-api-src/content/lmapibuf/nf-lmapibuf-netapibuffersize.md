---
UID: NF:lmapibuf.NetApiBufferSize
title: NetApiBufferSize function (lmapibuf.h)
description: The NetApiBufferSize function returns the size, in bytes, of a buffer allocated by a call to the NetApiBufferAllocate function.
helpviewer_keywords: ["NetApiBufferSize","NetApiBufferSize function [Network Management]","_win32_netapibuffersize","lmapibuf/NetApiBufferSize","netmgmt.netapibuffersize"]
old-location: netmgmt\netapibuffersize.htm
tech.root: NetMgmt
ms.assetid: 0c28feeb-00a3-4ad5-b85f-96326515fae2
ms.date: 12/05/2018
ms.keywords: NetApiBufferSize, NetApiBufferSize function [Network Management], _win32_netapibuffersize, lmapibuf/NetApiBufferSize, netmgmt.netapibuffersize
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
 - NetApiBufferSize
 - lmapibuf/NetApiBufferSize
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
 - NetApiBufferSize
---

# NetApiBufferSize function


## -description

The
				<b>NetApiBufferSize</b> function returns the size, in bytes, of a buffer allocated by a call to the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function.

## -parameters

### -param Buffer [in]

Pointer to a buffer returned by the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function.

### -param ByteCount [out]

Receives the size of the buffer, in bytes.

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