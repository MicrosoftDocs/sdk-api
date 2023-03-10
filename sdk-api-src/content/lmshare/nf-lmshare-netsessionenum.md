---
UID: NF:lmshare.NetSessionEnum
title: NetSessionEnum function (lmshare.h)
description: Provides information about sessions established on a server.
helpviewer_keywords: ["0","1","10","2","502","NetSessionEnum","NetSessionEnum function [Files]","_win32_netsessionenum","fs.netsessionenum","lmshare/NetSessionEnum","netmgmt.netsessionenum"]
old-location: fs\netsessionenum.htm
tech.root: fs
ms.assetid: 5923a8cc-bf7a-4ffa-b089-fd7f26ee42d2
ms.date: 12/05/2018
ms.keywords: 0, 1, 10, 2, 502, NetSessionEnum, NetSessionEnum function [Files], _win32_netsessionenum, fs.netsessionenum, lmshare/NetSessionEnum, netmgmt.netsessionenum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetSessionEnum
 - lmshare/NetSessionEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - srvcli.dll
api_name:
 - NetSessionEnum
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
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_0">SESSION_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer, name of the user, and open files, pipes, and devices on the computer. The <i>bufptr</i>  parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_1">SESSION_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
In addition to the information indicated for level 1, return the type of client and how the user established the session. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_2">SESSION_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer, name of the user, and active and idle times for the session. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_10">SESSION_INFO_10</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
Return the name of the computer; name of the user; open files, pipes, and devices on the computer; and the name of the transport the client is using. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_502">SESSION_INFO_502</a> structures.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter.

This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b>.

### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify <b>MAX_PREFERRED_LENGTH</b>, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b>. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

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
<b>NetSessionEnum</b> function at level 1 or level 2.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadssession">IADsSession</a> and 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations">IADsFileServiceOperations</a>.


#### Examples

The following code sample demonstrates how to retrieve information about current sessions using a call to the 
<b>NetSessionEnum</b> function. The sample calls 
<b>NetSessionEnum</b>, specifying information level 10 (
<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_10">SESSION_INFO_10</a>). The sample loops through the entries and prints the retrieved information. Finally, the code prints the total number of sessions enumerated and frees the memory allocated for the information buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "Netapi32.lib")

#include <stdio.h>
#include <assert.h>
#include <windows.h> 
#include <lm.h>

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
   if (argc > 4)
   {
      wprintf(L"Usage: %s [\\\\ServerName] [\\\\ClientName] [UserName]\n", argv[0]);
      exit(1);
   }

   if (argc >= 2)
      pszServerName = argv[1];

   if (argc >= 3)
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
                               (LPBYTE*)&pBuf,
                               dwPrefMaxLen,
                               &dwEntriesRead,
                               &dwTotalEntries,
                               &dwResumeHandle);
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
            for (i = 0; (i < dwEntriesRead); i++)
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
               wprintf(L"\n\tClient: %s\n", pTmpBuf->sesi10_cname);
               wprintf(L"\tUser:   %s\n", pTmpBuf->sesi10_username);
               printf("\tActive: %d\n", pTmpBuf->sesi10_time);
               printf("\tIdle:   %d\n", pTmpBuf->sesi10_idle_time);

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

```

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo">NetSessionGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_0">SESSION_INFO_0</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_1">SESSION_INFO_1</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_10">SESSION_INFO_10</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_2">SESSION_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-session_info_502">SESSION_INFO_502</a>



<a href="/windows/desktop/NetShare/session-functions">Session
		  Functions</a>
