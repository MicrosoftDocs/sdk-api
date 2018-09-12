---
UID: NF:lmserver.NetServerGetInfo
title: NetServerGetInfo function
author: windows-sdk-content
description: The NetServerGetInfo function retrieves current configuration information for the specified server.
old-location: netmgmt\netservergetinfo.htm
tech.root: netmgmt
ms.assetid: ed15e1b5-3fdc-4841-85d1-89269684df0e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 100, 101, 102, NetServerGetInfo, NetServerGetInfo function [Network Management], _win32_netservergetinfo, lmserver/NetServerGetInfo, netmgmt.netservergetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmserver.h
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
 - NetServerGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetServerGetInfo function


## -description


The
				<b>NetServerGetInfo</b> function retrieves current configuration information for the specified server.


## -parameters




### -param servername [in]

Pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="100"></a><dl>
<dt><b>100</b></dt>
</dl>
</td>
<td width="60%">
Return the server name and platform information. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/b027a669-b4d8-4d42-aedc-94834bf099da">SERVER_INFO_100</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="101"></a><dl>
<dt><b>101</b></dt>
</dl>
</td>
<td width="60%">
Return the server name, type, and associated software. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/6e106a51-9f0c-4603-8121-5b0d01a235b4">SERVER_INFO_101</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="102"></a><dl>
<dt><b>102</b></dt>
</dl>
</td>
<td width="60%">
Return the server name, type, associated software, and other attributes. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/4c63fee7-1103-414d-b650-da87f8184e91">SERVER_INFO_102</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. 




This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
</table>
 




## -remarks



Only the Administrators or Server Operators local group, or those with Print or Server Operator group membership, can successfully execute the 
<b>NetServerGetInfo</b> function at level 102. No special group membership is required for level 100 or level 101 calls.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions. For more information, see 
<a href="https://msdn.microsoft.com/e2b90a98-5777-42c2-95dd-4623e738c4da">IADsComputer</a>.


#### Examples

The following code sample demonstrates how to retrieve current configuration information for a server using a call to the 
<b>NetServerGetInfo</b> function. The sample calls 
<b>NetServerGetInfo</b>, specifying information level 101 (<a href="https://msdn.microsoft.com/6e106a51-9f0c-4603-8121-5b0d01a235b4">SERVER_INFO_101</a>). If the call succeeds, the code attempts to identify the type of server. Finally, the sample frees the memory allocated for the information buffer.

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

int wmain(int argc, wchar_t *argv[])
{
   DWORD dwLevel = 101;
   LPSERVER_INFO_101 pBuf = NULL;
   NET_API_STATUS nStatus;
   LPTSTR pszServerName = NULL;

   if (argc &gt; 2)
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName]\n", argv[0]);
      exit(1);
   }
   // The server is not the default local computer.
   //
   if (argc == 2)
      pszServerName = (LPTSTR) argv[1];
   //
   // Call the NetServerGetInfo function, specifying level 101.
   //
   nStatus = NetServerGetInfo(pszServerName,
                              dwLevel,
                              (LPBYTE *)&amp;pBuf);
   //
   // If the call succeeds,
   //
   if (nStatus == NERR_Success)
   {
      //
      // Check for the type of server.
      //
      if ((pBuf-&gt;sv101_type &amp; SV_TYPE_DOMAIN_CTRL) ||
         (pBuf-&gt;sv101_type &amp; SV_TYPE_DOMAIN_BAKCTRL) ||
         (pBuf-&gt;sv101_type &amp; SV_TYPE_SERVER_NT))
         printf("This is a server\n");
      else
         printf("This is a workstation\n");
   }
   //
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




<a href="https://msdn.microsoft.com/e807489a-250e-4d4c-adb6-eff8ac30603b">NetRemoteComputerSupports</a>



<a href="https://msdn.microsoft.com/1a04a43d-34f9-4a08-ac66-750120792af0">NetServerSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/b027a669-b4d8-4d42-aedc-94834bf099da">SERVER_INFO_100</a>



<a href="https://msdn.microsoft.com/6e106a51-9f0c-4603-8121-5b0d01a235b4">SERVER_INFO_101</a>



<a href="https://msdn.microsoft.com/4c63fee7-1103-414d-b650-da87f8184e91">SERVER_INFO_102</a>



<a href="https://msdn.microsoft.com/43e1285b-8c86-4af4-9834-fcd5ee8aceb8">Server
		  Functions</a>
 

 

