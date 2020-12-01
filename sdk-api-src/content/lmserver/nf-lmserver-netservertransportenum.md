---
UID: NF:lmserver.NetServerTransportEnum
title: NetServerTransportEnum function (lmserver.h)
description: The NetServerTransportEnum function supplies information about transport protocols that are managed by the server.
helpviewer_keywords: ["0","1","NetServerTransportEnum","NetServerTransportEnum function [Network Management]","_win32_netservertransportenum","lmserver/NetServerTransportEnum","netmgmt.netservertransportenum"]
old-location: netmgmt\netservertransportenum.htm
tech.root: NetMgmt
ms.assetid: db42ac44-d70d-4b89-882a-6ac83fd611fd
ms.date: 12/05/2018
ms.keywords: 0, 1, NetServerTransportEnum, NetServerTransportEnum function [Network Management], _win32_netservertransportenum, lmserver/NetServerTransportEnum, netmgmt.netservertransportenum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetServerTransportEnum
 - lmserver/NetServerTransportEnum
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
 - NetServerTransportEnum
---

## -description

The <b>NetServerTransportEnum</b> function supplies information about transport protocols that are managed by the server.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

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
Return information about the transport protocol, including name, address, and location on the network. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return information about the transport protocol, including name, address, network location, and domain. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a> structures.

</td>
</tr>
</table>

### -param bufptr [out]

Pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param prefmaxlen [in]

Specifies the preferred maximum length of returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

### -param entriesread [out]

Pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

Pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.

### -param resume_handle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing server transport search. The handle should be zero on the first call and left unchanged for subsequent calls. If this parameter is <b>NULL</b>, no resume handle is stored.

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
<dt><b>NERR_BufTooSmall</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is too small.

</td>
</tr>
</table>

## -remarks

Only Authenticated Users can successfully call this function.<b>Windows XP/2000:  </b>No special group membership is required to successfully execute this function.

## Examples

The following code sample demonstrates how to retrieve information about transport protocols that are managed by the server, using a call to the 
<b>NetServerTransportEnum</b> function. The sample calls 
<b>NetServerTransportEnum</b>, specifying information level 0 (
<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>). The sample prints the name of each transport protocol and the total number enumerated. Finally, the code sample frees the memory allocated for the information buffer.

```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <assert.h>
#include <windows.h> 
#include <lm.h>

int wmain(int argc, wchar_t *argv[])
{
   LPSERVER_TRANSPORT_INFO_0 pBuf = NULL;
   LPSERVER_TRANSPORT_INFO_0 pTmpBuf;
   DWORD dwLevel = 0;
   DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
   DWORD dwEntriesRead = 0;
   DWORD dwTotalEntries = 0;
   DWORD dwResumeHandle = 0;
   DWORD dwTotalCount = 0;
   NET_API_STATUS nStatus;
   LPTSTR pszServerName = NULL;
   DWORD i;

   if (argc > 2)
   {
      fwprintf(stderr, L"Usage: %s [\\\\ServerName]\n", argv[0]);
      exit(1);
   }
   // The server is not the default local computer.
   //
   if (argc == 2)
      pszServerName = (LPTSTR) argv[1];
   //
   // Call the NetServerTransportEnum function; specify level 0.
   //
   do // begin do
   {
      nStatus = NetServerTransportEnum(pszServerName,
                                       dwLevel,
                                       (LPBYTE *) &pBuf,
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
            // Loop through the entries;
            //  process access errors.
            //
            for (i = 0; i < dwEntriesRead; i++)
            {
               assert(pTmpBuf != NULL);

               if (pTmpBuf == NULL)
               {
                  fprintf(stderr, "An access violation has occurred\n");
                  break;
               }
               //
               // Print the transport protocol name. 
               //
               wprintf(L"\tTransport: %s\n", pTmpBuf->svti0_transportname);

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
      // Free the allocated buffer.
      //
      if (pBuf != NULL)
      {
         NetApiBufferFree(pBuf);
         pBuf = NULL;
      }
   // 
   // Continue to call NetServerTransportEnum while 
   //  there are more entries. 
   // 
   }
   while (nStatus == ERROR_MORE_DATA); // end do

   // Check again for an allocated buffer.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);
   //
   // Print the final count of transports enumerated.
   //
   fprintf(stderr, "\nTotal of %d entries enumerated\n", dwTotalCount);

   return 0;
}
```

## -see-also

<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>

<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>

<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_0">SERVER_TRANSPORT_INFO_0</a>

<a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_1">SERVER_TRANSPORT_INFO_1</a>

<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>
