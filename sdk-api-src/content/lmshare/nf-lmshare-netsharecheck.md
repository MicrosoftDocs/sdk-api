---
UID: NF:lmshare.NetShareCheck
title: NetShareCheck function (lmshare.h)
description: Checks whether or not a server is sharing a device.
helpviewer_keywords: ["NetShareCheck","NetShareCheck function [Files]","STYPE_DEVICE","STYPE_DISKTREE","STYPE_IPC","STYPE_PRINTQ","STYPE_SPECIAL","STYPE_TEMPORARY","_win32_netsharecheck","fs.netsharecheck","lmshare/NetShareCheck","netmgmt.netsharecheck"]
old-location: fs\netsharecheck.htm
tech.root: fs
ms.assetid: 8453dcd2-5c58-4fe4-9426-0fd51647394d
ms.date: 12/05/2018
ms.keywords: NetShareCheck, NetShareCheck function [Files], STYPE_DEVICE, STYPE_DISKTREE, STYPE_IPC, STYPE_PRINTQ, STYPE_SPECIAL, STYPE_TEMPORARY, _win32_netsharecheck, fs.netsharecheck, lmshare/NetShareCheck, netmgmt.netsharecheck
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
 - NetShareCheck
 - lmshare/NetShareCheck
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
 - NetShareCheck
---

# NetShareCheck function


## -description

Checks whether or not a server is sharing a device.

## -parameters

### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.

### -param device [in]

Pointer to a string that specifies the name of the device to check for shared access.

### -param type [out]

Pointer to a variable that receives a bitmask of flags that specify the type of the shared device. This parameter is set only if the function returns successfully. 

One of the following flags may be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_DISKTREE"></a><a id="stype_disktree"></a><dl>
<dt><b>STYPE_DISKTREE</b></dt>
</dl>
</td>
<td width="60%">
Disk drive.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_PRINTQ"></a><a id="stype_printq"></a><dl>
<dt><b>STYPE_PRINTQ</b></dt>
</dl>
</td>
<td width="60%">
Print queue.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_DEVICE"></a><a id="stype_device"></a><dl>
<dt><b>STYPE_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
Communication device.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_IPC"></a><a id="stype_ipc"></a><dl>
<dt><b>STYPE_IPC</b></dt>
</dl>
</td>
<td width="60%">
Interprocess communication (IPC).

</td>
</tr>
</table>
 

In addition, one or both of the following flags may be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="STYPE_SPECIAL"></a><a id="stype_special"></a><dl>
<dt><b>STYPE_SPECIAL</b></dt>
</dl>
</td>
<td width="60%">
Special share reserved for interprocess communication (IPC$) or remote administration of the server (ADMIN$). Can also refer to administrative shares such as C$, D$, E$, and so forth. For more information, see <a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="STYPE_TEMPORARY"></a><a id="stype_temporary"></a><dl>
<dt><b>STYPE_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
A temporary share.

</td>
</tr>
</table>

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
<dt><b>NERR_DeviceNotShared</b></dt>
</dl>
</td>
<td width="60%">
The device is not shared.

</td>
</tr>
</table>

## -remarks

This function applies only to Server Message Block (SMB) shares. For other types of shares, such as Distributed File System (DFS) or WebDAV shares, use <a href="/windows/desktop/WNet/windows-networking-functions">Windows Networking (WNet) functions</a>, which support all types of shares.

No special group membership is required to successfully execute the 
<b>NetShareCheck</b> function.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions. For more information, see 
<a href="/windows/desktop/api/iads/nn-iads-iadsfileshare">IADsFileShare</a>.


#### Examples

The following code sample demonstrates how to check whether a server is sharing a device, using a call to the 
<b>NetShareCheck</b> function. The function returns the type of device being shared, as described in the preceding documentation for the <i>type</i> parameter.


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include <lm.h>
#pragma comment(lib, "Netapi32.lib")

void wmain( int argc, TCHAR *argv[ ])
{
   NET_API_STATUS res;
   DWORD devType = 0;

   if(argc<3)
      printf("Usage: NetShareCheck server device\n");
   else
   {
      //
      // Call the NetShareCheck function.
      //
      res=NetShareCheck(argv[1], argv[2], &devType);
      //
      // If the function succeeds, inform the user.
      //
      if(res==0)
         printf("Device is shared as type %u.\n",devType);
      //
      // Otherwise, print the error.
      //
      else
         printf("Error: %u\n", res);
   }
   return;
}

```

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareenum">NetShareEnum</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>