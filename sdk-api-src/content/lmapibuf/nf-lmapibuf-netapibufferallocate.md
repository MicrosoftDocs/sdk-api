---
UID: NF:lmapibuf.NetApiBufferAllocate
title: NetApiBufferAllocate function
author: windows-sdk-content
description: The NetApiBufferAllocate function allocates memory from the heap. Use this function only when compatibility with the NetApiBufferFree function is required. Otherwise, use the memory management functions.
old-location: netmgmt\netapibufferallocate.htm
tech.root: netmgmt
ms.assetid: 9ff1e3eb-9417-469f-a8c0-cdcda3cd9583
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: NetApiBufferAllocate, NetApiBufferAllocate function [Network Management], _win32_netapibufferallocate, lmapibuf/NetApiBufferAllocate, netmgmt.netapibufferallocate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetApiBufferAllocate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetApiBufferAllocate function


## -description


The 
				<b>NetApiBufferAllocate</b> function allocates memory from the heap. Use this function only when compatibility with the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function is required. Otherwise, use the 
<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">memory management functions</a>.


## -parameters




### -param ByteCount [in]

Number of bytes to be allocated.


### -param Buffer [out]

Receives a pointer to the allocated buffer.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



No special group membership is required to successfully execute the ApiBuffer functions.

For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


#### Examples

The following code sample demonstrates how to use the network management 
<a href="https://msdn.microsoft.com/bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18">ApiBuffer functions</a>.

The sample first calls the 
<b>NetApiBufferAllocate</b> function to allocate memory and then the 
<a href="https://msdn.microsoft.com/0c28feeb-00a3-4ad5-b85f-96326515fae2">NetApiBufferSize</a> function to retrieve the size of the allocated memory. Following this, the sample calls 
<a href="https://msdn.microsoft.com/61153de0-33d3-4c83-a8aa-a7179252328c">NetApiBufferReallocate</a> to change the size of the memory allocation. Finally, the sample calls 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> to free the memory. In each case, the sample prints a message indicating success or failure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#include &lt;windows.h&gt;
#include &lt;lm.h&gt;
#include &lt;stdio.h&gt;

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
   res = NetApiBufferAllocate(1024, (LPVOID *) &amp;p);
   if(res == NERR_Success)
   {
      printf("NetApiBufferAllocate:   Allocated 1024 bytes.\n");

      // Call the NetApiBufferSize function 
      //   to retrieve the size of the allocated buffer.
      //   If successful, print the size.
      //
      res = NetApiBufferSize(p, &amp;dwSize);
      if(res == NERR_Success)
      {
         printf("NetApiBufferSize:       Buffer has %u bytes.\n", dwSize);

         // Call the NetApiBufferReallocate function
         //   to change the size of the allocated memory.
         //   If successful, print the new size of the buffer.
         //
         res = NetApiBufferReallocate(p, dwSize * 2, (LPVOID *) &amp;p);   
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18">Api Buffer
		  Functions</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>



<a href="https://msdn.microsoft.com/61153de0-33d3-4c83-a8aa-a7179252328c">NetApiBufferReallocate</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

