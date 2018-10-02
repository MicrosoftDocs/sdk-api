---
UID: NF:lmshare.NetShareGetInfo
title: NetShareGetInfo function
author: windows-sdk-content
description: Retrieves information about a particular shared resource on a server.
old-location: fs\netsharegetinfo.htm
tech.root: NetShare
ms.assetid: 672ea208-4048-4d2f-9606-ee3e2133765b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 0, 1, 1005, 2, 501, 502, 503, NetShareGetInfo, NetShareGetInfo function [Files], _win32_netsharegetinfo, fs.netsharegetinfo, lmshare/NetShareGetInfo, netmgmt.netsharegetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - NetShareGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetShareGetInfo function


## -description


Retrieves information about a particular shared resource on a server.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param netname [in]

Pointer to a string that specifies the name of the share for which to return information.


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
 Return the share name. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the shared resource, including the name and type of the resource, and a comment associated with the resource. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the shared resource, including name of the resource, type and permissions, password, and number of connections. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="501"></a><dl>
<dt><b>501</b></dt>
</dl>
</td>
<td width="60%">
 Return the name and type of the resource, and a comment associated with the resource. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/2900d84c-7357-4652-b8b3-c9734fcc0449">SHARE_INFO_501</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
 Return information about the shared resource, including name of the resource, type and permissions, number of connections, and other pertinent information. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure. If the <b>shi503_servername</b> member of this structure is "*", there is no configured server name.

<b>Windows Server 2003 and Windows XP:  </b>This information level is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="1005"></a><dl>
<dt><b>1005</b></dt>
</dl>
</td>
<td width="60%">
 Return a value that indicates whether the share is the root volume in a Dfs tree structure. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>. 




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
The value specified for the <i>level</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified parameter is not valid.

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
<tr>
<td width="40%">
<dl>
<dt><b>NERR_NetNameNotFound</b></dt>
</dl>
</td>
<td width="60%">
The share name does not exist.

</td>
</tr>
</table>
 




## -remarks



This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows Networking (WNet) functions</a>, which support all types of shares.

For interactive users (users who are logged on locally to the machine), no special group membership is required to execute the <b>NetShareGetInfo</b> function. For non-interactive users, Administrator, Power User, Print Operator, or Server Operator group membership is required to successfully execute the 
<a href="https://msdn.microsoft.com/9114c54d-3905-4d40-9162-b3ea605f6fcb">NetShareEnum</a> function at levels 2, 502, and 503. No special group membership is required for level 0 or level 1 calls.

<b>Windows Server 2003 and Windows XP:  </b>For all users, Administrator, Power User, Print Operator, or Server Operator group membership is required to successfully execute the 
<b>NetShareGetInfo</b> function at levels 2 and 502.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="https://msdn.microsoft.com/37695195-fc33-499d-98c1-ccfd190cb2f9">IADsFileShare</a>.

If 503 is specified for the <i>level</i> parameter, the remote server specified in the <b>shi503_servername</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure must have been bound to a transport protocol using the <a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.


#### Examples

The following code sample demonstrates how to retrieve information about a particular shared resource using a call to the 
<b>NetShareGetInfo</b> function. The sample calls 
<b>NetShareGetInfo</b>, specifying information level 502 (
<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>). If the call succeeds, the code prints the retrieved data. The sample also calls the 
<a href="https://msdn.microsoft.com/24a98229-11e4-45ef-988b-c2cf831275e7">IsValidSecurityDescriptor</a> function to validate the <b>shi502_security_descriptor</b> member. Finally, the sample frees the memory allocated for the information buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include <lm.h>

#pragma comment(lib, "Netapi32.lib")
#pragma comment(lib, "Advapi32.lib")

void wmain( int argc, TCHAR *lpszArgv[ ])
{
   PSHARE_INFO_502 BufPtr;
   NET_API_STATUS res;
   LPTSTR   lpszServer = NULL, lpszShare;
   //
   // Check command line arguments.
   //
   switch(argc)
   {
   case 3:
      lpszServer = lpszArgv[2];
   case 2:
      lpszShare = lpszArgv[1];
      break;
   default:
      printf("Usage: NetShareGetInfo sharename <servername>\n");
      return;
   }
   //
   // Call the NetShareGetInfo function, specifying level 502.
   //
   if((res = NetShareGetInfo (lpszServer,lpszShare,502,(LPBYTE *) &BufPtr)) == ERROR_SUCCESS)
   {
      //
      // Print the retrieved data.
      //
      printf("%S\t%S\t%u\n",BufPtr->shi502_netname, BufPtr->shi502_path, BufPtr->shi502_current_uses);
      //
      // Validate the value of the 
      //  shi502_security_descriptor member.
      //
      if (IsValidSecurityDescriptor(BufPtr->shi502_security_descriptor))
         printf("It has a valid Security Descriptor.\n");
      else
         printf("It does not have a valid Security Descriptor.\n");
      //
      // Free the allocated memory.
      //
      NetApiBufferFree(BufPtr);
   }
   else 
      printf("Error: %ld\n",res);
   return;
}

```





## -see-also




<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a>



<a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>



<a href="https://msdn.microsoft.com/9fb3e0ae-76b5-4432-80dd-f3361738aa7c">SHARE_INFO_1005</a>



<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>



<a href="https://msdn.microsoft.com/2900d84c-7357-4652-b8b3-c9734fcc0449">SHARE_INFO_501</a>



<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a>
 

 

