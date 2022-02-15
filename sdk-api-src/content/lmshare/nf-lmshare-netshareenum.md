---
UID: NF:lmshare.NetShareEnum
title: NetShareEnum function (lmshare.h)
description: Retrieves information about each shared resource on a server.
helpviewer_keywords: ["0","1","2","502","503","NetShareEnum","NetShareEnum function [Files]","_win32_netshareenum","fs.netshareenum","lmshare/NetShareEnum","netmgmt.netshareenum"]
old-location: fs\netshareenum.htm
tech.root: fs
ms.assetid: 9114c54d-3905-4d40-9162-b3ea605f6fcb
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 502, 503, NetShareEnum, NetShareEnum function [Files], _win32_netshareenum, fs.netshareenum, lmshare/NetShareEnum, netmgmt.netshareenum
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
 - NetShareEnum
 - lmshare/NetShareEnum
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
 - NetShareEnum
---

# NetShareEnum function


## -description

Retrieves information about each shared resource on a server.

You can also use the 
<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a> function to retrieve resource information. However, <b>WNetEnumResource</b> does not enumerate hidden shares or users connected to a share.

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
 Return share names. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return information about shared resources, including the name and type of the resource, and a comment associated with the resource. 


The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a> structures.
							

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
 Return information about shared resources, including name of the resource, type and permissions, password, and number of connections. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="502"></a><dl>
<dt><b>502</b></dt>
</dl>
</td>
<td width="60%">
 Return information about shared resources, including name of the resource, type and permissions, number of connections, and other pertinent information. The <i>bufptr</i> parameter points to an array of 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a> structures. Shares from different scopes are not returned. For more information about scoping, see the Remarks section of the documentation for the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Return information about shared resources, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>bufptr</i> parameter points to an array of <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structures. Shares from all scopes are returned. If the <b>shi503_servername</b> member of this structure is "*", there is no configured server name and the <b>NetShareEnum</b> function enumerates shares for all the unscoped names.

<b>Windows Server 2003 and Windows XP:  </b>This information level is not supported.

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

Pointer to a value that receives the total number of entries that could have been enumerated. Note that applications should consider this value only as a hint.

### -param resume_handle [in, out]

Pointer to a value that contains a resume handle which is used to continue an existing share search. The handle should be zero on the first call and left unchanged for subsequent calls. If <i>resume_handle</i> is <b>NULL</b>, then no resume handle is stored.

## -returns

If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="/windows/desktop/WNet/windows-networking-functions">Windows Networking (WNet) functions</a>, which support all types of shares.

For interactive users (users who are logged on locally to the machine), no special group membership is required to execute the <b>NetShareEnum</b> function. For non-interactive users, Administrator, Power User, Print Operator, or Server Operator group membership is required to successfully execute the 
<b>NetShareEnum</b> function at levels 2, 502, and 503. No special group membership is required for level 0 or level 1 calls.

<b>Windows Server 2022:  </b> For non-interactive users, Administrator, Access Control Assistance Operators, or Server Operator group membership is required to successfully execute the 
<b>NetShareEnum</b> function at levels 2, 502, and 503.

<b>Windows Server 2003 and Windows XP:  </b>For all users, Administrator, Power User, Print Operator, or Server Operator group membership is required to successfully execute the 
<b>NetShareEnum</b> function at levels 2 and 502.

To retrieve a value that indicates whether a share is the root volume in a DFS tree structure, you must call the 
<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a> function and specify information level 1005.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileshare">IADsFileShare</a>.


#### Examples

The following code sample demonstrates how to retrieve information about each shared resource on a server using a call to the 
<b>NetShareEnum</b> function. The sample calls 
<b>NetShareEnum</b>, specifying information level 502 (<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>). If the call succeeds, the code loops through the entries and prints information about each share. The sample also calls the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsecuritydescriptor">IsValidSecurityDescriptor</a> function to validate the <b>shi502_security_descriptor</b> member. Finally, the code sample frees the memory allocated for the information buffer.


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
   PSHARE_INFO_502 BufPtr,p;
   NET_API_STATUS res;
   LPTSTR   lpszServer = NULL;
   DWORD er=0,tr=0,resume=0, i;

   switch(argc)
   {
   case 2:
      lpszServer = lpszArgv[1];
      break;
   default:
      printf("Usage: NetShareEnum <servername>\n");
      return;
   }
   //
   // Print a report header.
   //
   printf("Share:              Local Path:                   Uses:   Descriptor:\n");
   printf("---------------------------------------------------------------------\n");
   //
   // Call the NetShareEnum function; specify level 502.
   //
   do // begin do
   {
      res = NetShareEnum (lpszServer, 502, (LPBYTE *) &BufPtr, MAX_PREFERRED_LENGTH, &er, &tr, &resume);
      //
      // If the call succeeds,
      //
      if(res == ERROR_SUCCESS || res == ERROR_MORE_DATA)
      {
         p=BufPtr;
         //
         // Loop through the entries;
         //  print retrieved data.
         //
         for(i=1;i<=er;i++)
         {
            printf("%-20S%-30S%-8u",p->shi502_netname, p->shi502_path, p->shi502_current_uses);
            //
            // Validate the value of the 
            //  shi502_security_descriptor member.
            //
            if (IsValidSecurityDescriptor(p->shi502_security_descriptor))
               printf("Yes\n");
            else
               printf("No\n");
            p++;
         }
         //
         // Free the allocated buffer.
         //
         NetApiBufferFree(BufPtr);
      }
      else 
         printf("Error: %ld\n",res);
   }
   // Continue to call NetShareEnum while 
   //  there are more entries. 
   // 
   while (res==ERROR_MORE_DATA); // end do
   return;
}

```

## -see-also

<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>
