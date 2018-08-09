---
UID: NF:lmshare.NetSessionEnum
title: NetSessionEnum function
author: windows-sdk-content
description: Provides information about sessions established on a server.
old-location: fs\netsessionenum.htm
old-project: netshare
ms.assetid: 5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0, 1, 10, 2, 502, NetSessionEnum, NetSessionEnum function [Files], _win32_netsessionenum, fs.netsessionenum, lmshare/NetSessionEnum, netmgmt.netsessionenum
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, *LPSERVER_TRANSPORT_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetSessionEnum
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetSessionEnum function


## -description


Provides information about sessions established on a server.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 



					


### -param UncClientName [in]

Pointer to a string that specifies the name of the computer session for which information is to be returned. If this parameter is <b>NULL</b>, 
<b>NetSessionEnum</b> returns information for all computer sessions on the server.


### -param username [in]

Pointer to a string that specifies the name of the user for which information is to be returned. If this parameter is <b>NULL</b>, 
<b>NetSessionEnum</b> returns information for all users.


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
Return the name of the computer that established the session. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/6b39df47-f25c-41dd-ba15-6e6806c4ec89">SESSION_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer, name of the user, and open files, pipes, and devices on the computer. The <i>bufptr</i>  parameter points to an array of 
<a href="https://msdn.microsoft.com/bc1c985e-b8af-4134-9ae4-511d82e3909b">SESSION_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
In addition to the information indicated for level 1, return the type of client and how the user established the session. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/c3429eba-4277-4dc7-9255-cd2ff18dc583">SESSION_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer, name of the user, and active and idle times for the session. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/a23a5647-f99d-4cb8-9d84-93653a3e7428">SESSION_INFO_10</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer; name of the user; open files, pipes, and devices on the computer; and the name of the transport the client is using. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/a86a00ae-f60a-4b12-a9ac-4b96f9abd6a2">SESSION_INFO_502</a> structures.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter.

This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b>.


### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify <b>MAX_PREFERRED_LENGTH</b>, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b>. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.


### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.


### -param resume_handle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing session search. The handle should be zero on the first call and left unchanged for subsequent calls. If <i>resume_handle</i> is <b>NULL</b>, no resume handle is stored.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

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
<dt><b>NERR_ClientNameNotFound</b></dt>
</dl>
</td>
<td width="60%">
A session does not exist with the computer name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The computer name is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_UserNotFound</b></dt>
</dl>
</td>
<td width="60%">
The user name could not be found.

</td>
</tr>
</table>
 




## -remarks



Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetSessionEnum</b> function at level 1 or level 2. No special group membership is required for level 0 or level 10 calls.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions. For more information, see 
<a href="https://msdn.microsoft.com/54621f0d-7478-4a6f-a96f-f3f93e64b281">IADsSession</a> and 
<a href="https://msdn.microsoft.com/91335658-8efb-4945-9862-f72e78d749d6">IADsFileServiceOperations</a>.


#### Examples

The following code sample demonstrates how to retrieve information about current sessions using a call to the 
<b>NetSessionEnum</b> function. The sample calls 
<b>NetSessionEnum</b>, specifying information level 10 (
<a href="https://msdn.microsoft.com/a23a5647-f99d-4cb8-9d84-93653a3e7428">SESSION_INFO_10</a>). The sample loops through the entries and prints the retrieved information. Finally, the code prints the total number of sessions enumerated and frees the memory allocated for the information buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "Netapi32.lib")

#include &lt;stdio.h&gt;
#include &lt;assert.h&gt;
#include &lt;windows.h&gt; 
#include &lt;lm.h&gt;

int wmain(int argc, wchar_t *argv[])
{
   LPSESSION_INFO_10 pBuf = NULL;
   LPSESSION_INFO_10 pTmpBuf;
   DWORD dwLevel = 10;
   DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
   DWORD dwEntriesRead = 0;
   DWORD dwTotalEntries = 0;
   DWORD dwResumeHandle = 0;
   DWORD i;
   DWORD dwTotalCount = 0;
   LPTSTR pszServerName = NULL;
   LPTSTR pszClientName = NULL;
   LPTSTR pszUserName = NULL;
   NET_API_STATUS nStatus;
   //
   // Check command line arguments.
   //
   if (argc &gt; 4)
   {
      wprintf(L"Usage: %s [\\\\ServerName] [\\\\ClientName] [UserName]\n", argv[0]);
      exit(1);
   }

   if (argc &gt;= 2)
      pszServerName = argv[1];

   if (argc &gt;= 3)
      pszClientName = argv[2];

   if (argc == 4)
      pszUserName = argv[3];
   //
   // Call the NetSessionEnum function, specifying level 10.
   //
   do // begin do
   {
      nStatus = NetSessionEnum(pszServerName,
                               pszClientName,
                               pszUserName,
                               dwLevel,
                               (LPBYTE*)&amp;pBuf,
                               dwPrefMaxLen,
                               &amp;dwEntriesRead,
                               &amp;dwTotalEntries,
                               &amp;dwResumeHandle);
      //
      // If the call succeeds,
      //
      if ((nStatus == NERR_Success) || (nStatus == ERROR_MORE_DATA))
      {
         if ((pTmpBuf = pBuf) != NULL)
         {
            //
            // Loop through the entries.
            //
            for (i = 0; (i &lt; dwEntriesRead); i++)
            {
               assert(pTmpBuf != NULL);

               if (pTmpBuf == NULL)
               {
                  fprintf(stderr, "An access violation has occurred\n");
                  break;
               }
               //
               // Print the retrieved data. 
               //
               wprintf(L"\n\tClient: %s\n", pTmpBuf-&gt;sesi10_cname);
               wprintf(L"\tUser:   %s\n", pTmpBuf-&gt;sesi10_username);
               printf("\tActive: %d\n", pTmpBuf-&gt;sesi10_time);
               printf("\tIdle:   %d\n", pTmpBuf-&gt;sesi10_idle_time);

               pTmpBuf++;
               dwTotalCount++;
            }
         }
      }
      //
      // Otherwise, indicate a system error.
      //
      else
         fprintf(stderr, "A system error has occurred: %d\n", nStatus);
      //
      // Free the allocated memory.
      //
      if (pBuf != NULL)
      {
         NetApiBufferFree(pBuf);
         pBuf = NULL;
      }
   }
   // 
   // Continue to call NetSessionEnum while 
   //  there are more entries. 
   // 
   while (nStatus == ERROR_MORE_DATA); // end do

   // Check again for an allocated buffer.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);
   //
   // Print the final count of sessions enumerated.
   //
   fprintf(stderr, "\nTotal of %d entries enumerated\n", dwTotalCount);

   return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d44fb8d8-2b64-4268-8603-7784e2c5f2d5">NetSessionGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/6b39df47-f25c-41dd-ba15-6e6806c4ec89">SESSION_INFO_0</a>



<a href="https://msdn.microsoft.com/bc1c985e-b8af-4134-9ae4-511d82e3909b">SESSION_INFO_1</a>



<a href="https://msdn.microsoft.com/a23a5647-f99d-4cb8-9d84-93653a3e7428">SESSION_INFO_10</a>



<a href="https://msdn.microsoft.com/c3429eba-4277-4dc7-9255-cd2ff18dc583">SESSION_INFO_2</a>



<a href="https://msdn.microsoft.com/a86a00ae-f60a-4b12-a9ac-4b96f9abd6a2">SESSION_INFO_502</a>



<a href="https://msdn.microsoft.com/931455e3-1301-4a68-93c3-2674b3d4c491">Session
		  Functions</a>
 

 

