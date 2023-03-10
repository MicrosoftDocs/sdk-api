---
UID: NF:lmserver.NetServerDiskEnum
title: NetServerDiskEnum function (lmserver.h)
description: The NetServerDiskEnum function retrieves a list of disk drives on a server. The function returns an array of three-character strings (a drive letter, a colon, and a terminating null character).
helpviewer_keywords: ["NetServerDiskEnum","NetServerDiskEnum function [Network Management]","_win32_netserverdiskenum","lmserver/NetServerDiskEnum","netmgmt.netserverdiskenum"]
old-location: netmgmt\netserverdiskenum.htm
tech.root: NetMgmt
ms.assetid: 56c981f4-7a1d-4465-bd7b-5996222c4210
ms.date: 12/05/2018
ms.keywords: NetServerDiskEnum, NetServerDiskEnum function [Network Management], _win32_netserverdiskenum, lmserver/NetServerDiskEnum, netmgmt.netserverdiskenum
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
 - NetServerDiskEnum
 - lmserver/NetServerDiskEnum
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
 - NetServerDiskEnum
---

# NetServerDiskEnum function


## -description

The
				<b>NetServerDiskEnum</b> function retrieves a list of disk drives on a server. The function returns an array of three-character strings (a drive letter, a colon, and a terminating null character).

## -parameters

### -param servername [in]

A pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param level [in]

The level of information required. A value of zero is the only valid level.

### -param bufptr [out]

A pointer to the buffer that receives the data. The data is an array of three-character strings (a drive letter, a colon, and a terminating null character). This buffer is allocated by the system and must be freed using the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA.

### -param prefmaxlen [in]

The preferred maximum length of returned data, in bytes. If you specify MAX_PREFERRED_LENGTH, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns ERROR_MORE_DATA. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>. 

<div class="alert"><b>Note</b>  This parameter is currently ignored.</div>
<div> </div>

### -param entriesread [out]

A pointer to a value that receives the count of elements actually enumerated.

### -param totalentries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.

### -param resume_handle [in, out]

A pointer to a value that contains a resume handle which is used to continue an existing server disk search. The handle should be zero on the first call and left unchanged for subsequent calls. If the <i>resume_handle</i> parameter is a <b>NULL</b> pointer, then no resume handle is stored.

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
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if a remote server was specified in <i>servername</i> parameter, the remote server only supports remote RPC calls using the legacy Remote Access Protocol mechanism, and this request is not supported. 

</td>
</tr>
</table>

## -remarks

Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerDiskEnum</b> function on a remote computer.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same results you can achieve by calling the network management server functions. For more information, see 
the <a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a> interface reference.


#### Examples

The following code sample demonstrates how to call the 
<b>NetServerDiskEnum</b> function to retrieve a list of disk drives on a server. The sample calls 
<b>NetServerDiskEnum</b>, specifying the information level 0 (required). If there are entries to return, and the user has access to the information, it prints a list of the drives, in the format of a three-character string: a drive letter, a colon, and a terminating null character. The sample also prints the total number of entries that are available and a hint about the number of entries actually enumerated. Finally, the code sample frees the memory allocated for the buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <stdio.h>
#include <assert.h>
#include <windows.h> 
#include <lm.h>

#pragma comment(lib, "netapi32.lib")

int wmain(int argc, wchar_t *argv[])
{
   const int ENTRY_SIZE = 3; // Drive letter, colon, NULL
   LPTSTR pBuf = NULL;
   DWORD dwLevel = 0; // level must be zero
   DWORD dwPrefMaxLen = MAX_PREFERRED_LENGTH;
   DWORD dwEntriesRead = 0;
   DWORD dwTotalEntries = 0;
   NET_API_STATUS nStatus;
   LPWSTR pszServerName = NULL;

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
   // Call the NetServerDiskEnum function.
   //
   nStatus = NetServerDiskEnum(pszServerName,
                               dwLevel,
                               (LPBYTE *) &pBuf,
                               dwPrefMaxLen,
                               &dwEntriesRead,
                               &dwTotalEntries,
                               NULL);
   //
   // If the call succeeds,
   //
   if (nStatus == NERR_Success)
   {
      LPTSTR pTmpBuf;

      if ((pTmpBuf = pBuf) != NULL)
      {
         DWORD i;
         DWORD dwTotalCount = 0;
         //
         // Loop through the entries.
         //
         for (i = 0; i < dwEntriesRead; i++)
         {
            assert(pTmpBuf != NULL);

            if (pTmpBuf == NULL)
            {
               // On a remote computer, only members of the
               //  Administrators or the Server Operators 
               //  local group can execute NetServerDiskEnum.
               //
               fprintf(stderr, "An access violation has occurred\n");
               break;
            }
            //
            // Print drive letter, colon, NULL for each drive;
            //   the number of entries actually enumerated; and
            //   the total number of entries available.
            //
            fwprintf(stdout, L"\tDisk: %S\n", pTmpBuf);

            pTmpBuf += ENTRY_SIZE;
            dwTotalCount++;
         }

         fprintf(stderr, "\nEntries enumerated: %d\n", dwTotalCount);
      }
   }
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   //
   // Free the allocated buffer.
   //
   if (pBuf != NULL)
      NetApiBufferFree(pBuf);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadscomputer">IADsComputer</a>



<a href="/windows/desktop/api/lmserver/nf-lmserver-netserverenum">NetServerEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/server-functions">Server
		  Functions</a>