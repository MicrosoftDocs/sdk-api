---
UID: NF:lmaccess.NetAccessDel
title: NetAccessDel function
author: windows-sdk-content
description: Not supported.
old-location: netmgmt\netaccessdel.htm
old-project: netmgmt
ms.assetid: be33d9b4-9740-4ccb-ac95-25ae02edaa42
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NetAccessDel, NetAccessDel function [Network Management], _win32_netaccessdel, lmaccess/NetAccessDel, netmgmt.netaccessdel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmaccess.h
req.include-header: Lm.h, Lmaccess.h
req.redist: 
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
tech.root: 
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetAccessDel
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetAccessDel function


## -description


<p class="CCE_Message">[This function is obsolete. For a list of alternate functions, see <a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Authorization Functions</a>.]

Not supported.

 The 
<b>NetAccessDel</b> function deletes the access control list (ACL) for a resource.


## -parameters




### -param servername

TBD


### -param resource

Pointer to a string that contains the name of the network resource for which to remove the access control list.


#### - pszServer

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



This function requires Admin privilege to successfully execute on a computer that has local security enabled.




## -see-also




<a href="https://msdn.microsoft.com/c236f335-b5de-4e8b-851d-45e008791271">Authorization Functions</a>
 

 

