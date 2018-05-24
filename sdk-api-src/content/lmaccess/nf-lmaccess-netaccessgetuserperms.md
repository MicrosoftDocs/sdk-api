---
UID: NF:lmaccess.NetAccessGetUserPerms
title: NetAccessGetUserPerms function
author: windows-driver-content
description: Not supported.
old-location: netmgmt\netaccessgetuserperms.htm
old-project: NetMgmt
ms.assetid: 8f4f069f-86d7-40cf-a821-32345d308f70
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: NetAccessGetUserPerms, NetAccessGetUserPerms function [Network Management], _win32_netaccessgetuserperms, lmaccess/NetAccessGetUserPerms, netmgmt.netaccessgetuserperms
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmaccess.h
req.include-header: Lm.h, Lmaccess.h
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
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetAccessGetUserPerms
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetAccessGetUserPerms function


## -description


<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Authorization Functions</a>.]

Not supported.

 The 
<b>NetAccessGetUserPerms</b> function returns a specified user's or group's access permissions for a particular resource.


## -parameters




### -param OPTIONAL

TBD


### -param UGname

TBD


### -param resource

TBD


### -param Perms

TBD




#### - pszResource

Pointer to a string that contains the name of the network resource to query.


#### - pszServer

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


#### - pszUgName

Pointer to a string that specifies the name of the user or group to query.


#### - pusPerms

Pointer to an unsigned short integer that receives the user permissions for the specified resource.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



This function requires Admin privilege to successfully execute on a computer that has local security enabled. When users request their own access permissions, no special privilege is required.




## -see-also




<a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Authorization Functions</a>
 

 

