---
UID: NF:lmwksta.NetWkstaUserSetInfo
title: NetWkstaUserSetInfo function (lmwksta.h)
description: The NetWkstaUserSetInfo function sets the user-specific information about the configuration elements for a workstation.
helpviewer_keywords: ["1","1101","NetWkstaUserSetInfo","NetWkstaUserSetInfo function [Network Management]","_win32_netwkstausersetinfo","lmwksta/NetWkstaUserSetInfo","netmgmt.netwkstausersetinfo"]
old-location: netmgmt\netwkstausersetinfo.htm
tech.root: NetMgmt
ms.assetid: d48667a3-5ae9-4a7d-9af6-14f08835940d
ms.date: 12/05/2018
ms.keywords: 1, 1101, NetWkstaUserSetInfo, NetWkstaUserSetInfo function [Network Management], _win32_netwkstausersetinfo, lmwksta/NetWkstaUserSetInfo, netmgmt.netwkstausersetinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetWkstaUserSetInfo
 - lmwksta/NetWkstaUserSetInfo
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
 - NetWkstaUserSetInfo
---

# NetWkstaUserSetInfo function


## -description

The
				<b>NetWkstaUserSetInfo</b> function sets the user-specific information about the configuration elements for a workstation.

## -parameters

### -param reserved

This parameter must be set to zero.

### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the workstation, including the name of the current user and the domains accessed by the workstation. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_user_info_1">WKSTA_USER_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="1101"></a><dl>
<dt><b>1101</b></dt>
</dl>
</td>
<td width="60%">
Specifies domains browsed by the workstation. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_user_info_1101">WKSTA_USER_INFO_1101</a> structure.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

### -param parm_err [out]

Pointer to a value that receives the index of the first parameter that causes the ERROR_INVALID_PARAMETER error. If this parameter is <b>NULL</b>, the index is not returned on error.

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
<b>NetWkstaUserSetInfo</b> function only works locally. Administrator group membership is required.

Domain names in the <b>wkui1101_oth_domains</b> member of the 
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_user_info_1101">WKSTA_USER_INFO_1101</a> structure are separated by spaces. An empty list is valid. A <b>NULL</b> pointer means to leave the member unmodified. The <b>wkui1101_oth_domains</b> member cannot be set with MS-DOS. When setting this element, 
<b>NetWkstaUserSetInfo</b> rejects the request if the name list was invalid or if a name could not be added to one or more of the network adapters managed by the system.

If the 
<b>NetWkstaUserSetInfo</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>parm_err</i> parameter to indicate the member of the workstation user information structure that is invalid. (A workstation user information structure begins with WKSTA_USER_INFO_ and its format is specified by the <i>level</i> parameter.) The following table lists the value that can be returned in the <i>parm_err</i> parameter and the corresponding structure member that is in error. (The prefix wkui*_ indicates that the member can begin with multiple prefixes, for example, wkui0_ or wkui1_.)

<table>
<tr>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>WKSTA_OTH_DOMAINS_PARMNUM</td>
<td>wkui*_oth_domains</td>
</tr>
</table>
 


#### Examples

The following code sample demonstrates how to set user-specific information for a workstation using a call to the 
<b>NetWkstaUserSetInfo</b> function, specifying information level 1101 (
<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_user_info_1101">WKSTA_USER_INFO_1101</a>).


```cpp
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "netapi32.lib")

#include <stdio.h>
#include <windows.h> 
#include <lm.h>

int wmain(int argc, wchar_t *argv[])
{
   DWORD dwLevel = 1101;
   WKSTA_USER_INFO_1101 wui;
   NET_API_STATUS nStatus;

   if (argc != 2)
   {
      fwprintf(stderr, L"Usage: %s OtherDomains\n", argv[0]);
      exit(1);
   }
   //
   // Fill in the WKSTA_USER_INFO_1101 structure member.
   //
   wui.wkui1101_oth_domains = argv[1];
   //
   // Call the NetWkstaUserSetInfo function
   //  to change the list of domains browsed by
   //  the workstation; specify level 1101.
   //
   nStatus = NetWkstaUserSetInfo(NULL,
                                 dwLevel,
                                 (LPBYTE)&wui,
                                 NULL);
   //
   // Display the result of the call.
   //
   if (nStatus == NERR_Success)
      fprintf(stderr, "Workstation user information has been changed\n");
   else
      fprintf(stderr, "A system error has occurred: %d\n", nStatus);

   return 0;
}

```

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstausergetinfo">NetWkstaUserGetInfo</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_user_info_1">WKSTA_USER_INFO_1</a>



<a href="/windows/desktop/api/lmwksta/ns-lmwksta-wksta_user_info_1101">WKSTA_USER_INFO_1101</a>



<a href="/windows/desktop/NetMgmt/workstation-and-workstation-user-functions">Workstation and Workstation User Functions</a>