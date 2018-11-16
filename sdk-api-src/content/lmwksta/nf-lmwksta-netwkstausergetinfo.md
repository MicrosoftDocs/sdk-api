---
UID: NF:lmwksta.NetWkstaUserGetInfo
title: NetWkstaUserGetInfo function
author: windows-sdk-content
description: The NetWkstaUserGetInfo function returns information about the currently logged-on user. This function must be called in the context of the logged-on user.
old-location: netmgmt\netwkstausergetinfo.htm
tech.root: NetMgmt
ms.assetid: 25ec7a49-fd26-4105-823b-a257a57f724e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 0, 1, 1101, NetWkstaUserGetInfo, NetWkstaUserGetInfo function [Network Management], _win32_netwkstausergetinfo, lmwksta/NetWkstaUserGetInfo, netmgmt.netwkstausergetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmwksta.h
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
 - NetWkstaUserGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NetWkstaUserGetInfo
: 
---

# NetWkstaUserGetInfo function


## -description


The
				<b>NetWkstaUserGetInfo</b> function returns information about the currently logged-on user. This function must be called in the context of the logged-on user.


## -parameters




### -param reserved

This parameter must be set to <b>NULL</b>.


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the user currently logged on to the workstation. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/8bd8d8c7-4558-46cb-ab46-a2197d53e9f7">WKSTA_USER_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return information about the workstation, including the name of the current user and the domains accessed by the workstation. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/a30747de-6cb0-41dc-95a7-be3d471056d5">WKSTA_USER_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1101"></a><dl>
<dt><b>1101</b></dt>
</dl>
</td>
<td width="60%">
Return domains browsed by the workstation. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/88772ba2-046b-4b03-ae02-d851075e4363">WKSTA_USER_INFO_1101</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>bufptr</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system ran out of memory resources. Either the network manager configuration is incorrect, or the program is running on a system with insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the function parameters is invalid.

</td>
</tr>
</table>
 




## -remarks



The 
<b>NetWkstaUserGetInfo</b> function only works locally.


#### Examples

The following code sample demonstrates how to retrieve information about the currently logged-on user using a call to the 
<b>NetWkstaUserGetInfo</b> function. The sample calls 
<b>NetWkstaUserGetInfo</b>, specifying information level 1 (
<a href="https://msdn.microsoft.com/a30747de-6cb0-41dc-95a7-be3d471056d5">WKSTA_USER_INFO_1</a>). If the call succeeds, the sample prints information about the logged-on user. Finally, the sample frees the memory allocated for the information buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include &lt;stdio.h&gt;
#include &lt;windows.h&gt; 
#include &lt;lm.h&gt;

int wmain(void)
{
   DWORD dwLevel = 1;
   LPWKSTA_USER_INFO_1 pBuf = NULL;
   NET_API_STATUS nStatus;
   //
   // Call the NetWkstaUserGetInfo function;
   //  specify level 1.
   //
   nStatus = NetWkstaUserGetInfo(NULL,
                                 dwLevel,
                                 (LPBYTE *)&amp;pBuf);
   //
   // If the call succeeds, print the information
   //  about the logged-on user.
   //
   if (nStatus == NERR_Success)
   {
      if (pBuf != NULL)
      {
         wprintf(L"\n\tUser:          %s\n", pBuf-&gt;wkui1_username);
         wprintf(L"\tDomain:        %s\n", pBuf-&gt;wkui1_logon_domain);
         wprintf(L"\tOther Domains: %s\n", pBuf-&gt;wkui1_oth_domains);
         wprintf(L"\tLogon Server:  %s\n", pBuf-&gt;wkui1_logon_server);
      }
   }
   // Otherwise, print the system error.
   //
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);
   //
   // Free the allocated memory.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);

   return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d746b6c9-5ef1-4174-a84f-44e4e50200cd">NetWkstaSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/8bd8d8c7-4558-46cb-ab46-a2197d53e9f7">WKSTA_USER_INFO_0</a>



<a href="https://msdn.microsoft.com/a30747de-6cb0-41dc-95a7-be3d471056d5">WKSTA_USER_INFO_1</a>



<a href="https://msdn.microsoft.com/88772ba2-046b-4b03-ae02-d851075e4363">WKSTA_USER_INFO_1101</a>



<a href="https://msdn.microsoft.com/cc400f43-297b-4ff4-8353-b268839c48b8">Workstation and Workstation User Functions</a>
 

 

