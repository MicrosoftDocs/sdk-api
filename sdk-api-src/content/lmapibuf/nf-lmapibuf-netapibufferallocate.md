---
UID: NF:lmapibuf.NetApiBufferAllocate
title: NetApiBufferAllocate function (lmapibuf.h)
description: The NetApiBufferAllocate function allocates memory from the heap. Use this function only when compatibility with the NetApiBufferFree function is required. Otherwise, use the memory management functions.
helpviewer_keywords: ["NetApiBufferAllocate","NetApiBufferAllocate function [Network Management]","_win32_netapibufferallocate","lmapibuf/NetApiBufferAllocate","netmgmt.netapibufferallocate"]
old-location: netmgmt\netapibufferallocate.htm
tech.root: NetMgmt
ms.assetid: 9ff1e3eb-9417-469f-a8c0-cdcda3cd9583
ms.date: 12/05/2018
ms.keywords: NetApiBufferAllocate, NetApiBufferAllocate function [Network Management], _win32_netapibufferallocate, lmapibuf/NetApiBufferAllocate, netmgmt.netapibufferallocate
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
 - NetApiBufferAllocate
 - lmapibuf/NetApiBufferAllocate
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
 - NetApiBufferAllocate
---

# NetApiBufferAllocate function


## -description

The 
				<b>NetApiBufferAllocate</b> function allocates memory from the heap. Use this function only when compatibility with the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function is required. Otherwise, use the 
<a href="/windows/desktop/Memory/memory-management-functions">memory management functions</a>.

## -parameters

### -param ByteCount [in]

Number of bytes to be allocated.

### -param Buffer [out]

Receives a pointer to the allocated buffer.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required to successfully execute the ApiBuffer functions.

For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.


#### Examples

The following code sample demonstrates how to use the network management 
<a href="/windows/desktop/NetMgmt/apibuffer-functions">ApiBuffer functions</a>.

The sample first calls the 
<b>NetApiBufferAllocate</b> function to allocate memory and then the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibuffersize">NetApiBufferSize</a> function to retrieve the size of the allocated memory. Following this, the sample calls 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferreallocate">NetApiBufferReallocate</a> to change the size of the memory allocation. Finally, the sample calls 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> to free the memory. In each case, the sample prints a message indicating success or failure.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

void PrintError(LPSTR lpszApi, DWORD res);

int main()
{
   PUSER_INFO_10 p;
   DWORD res, dwSize;

   // Call the NetApiBufferAllocate function 
   //   to allocate the memory. If successful,
   //   print a message.
   //
   res = NetApiBufferAllocate(1024, (LPVOID *) &p);
   if(res == NERR_Success)
   {
      printf("NetApiBufferAllocate:   Allocated 1024 bytes.\n");

      // Call the NetApiBufferSize function 
      //   to retrieve the size of the allocated buffer.
      //   If successful, print the size.
      //
      res = NetApiBufferSize(p, &dwSize);
      if(res == NERR_Success)
      {
         printf("NetApiBufferSize:       Buffer has %u bytes.\n", dwSize);

         // Call the NetApiBufferReallocate function
         //   to change the size of the allocated memory.
         //   If successful, print the new size of the buffer.
         //
         res = NetApiBufferReallocate(p, dwSize * 2, (LPVOID *) &p);   
         if(res == NERR_Success)
            printf("NetApiBufferReallocate: Re-Allocated %u bytes.\n", dwSize * 2);
         else
            PrintError("NetApiBufferReallocate", res);

         // Call the NetApiBufferFree function
         //    to free the allocated memory.
         //    If successful, print a message.
         //
         res = NetApiBufferFree(p);
         if(res == NERR_Success)
            printf("Freed Buffer\n");

         else
            PrintError("NetApiBufferFree", res);
      }
      else
         PrintError("NetApiBufferSize", res);
   }         
   else
      PrintError("NetApiBufferAllocate", res);
   return 0;
}

void PrintError(LPSTR lpszApi, DWORD res)
{
   printf("%s: Error %u\n", lpszApi, res);
   return;
}

```

## -see-also

<a href="/windows/desktop/NetMgmt/apibuffer-functions">Api Buffer
		  Functions</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferreallocate">NetApiBufferReallocate</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>