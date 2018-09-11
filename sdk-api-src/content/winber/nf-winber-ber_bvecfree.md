---
UID: NF:winber.ber_bvecfree
title: ber_bvecfree function
author: windows-sdk-content
description: The ber_bvecfree function frees an array of berval structures.
old-location: ldap\ber_bvecfree.htm
tech.root: ldap
ms.assetid: 5c2b53e4-257e-4c3f-b712-345e6b33341b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ber_bvecfree, ber_bvecfree, ber_bvecfree function [LDAP], ldap.ber__bvecfree, ldap.ber_bvecfree, winber/ber_bvecfree"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winber.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ber_bvecfree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ber_bvecfree function


## -description


The <b>ber_bvecfree</b> function frees an array of 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures.


## -parameters




### -param pBerVal [in]

Pointer to a NULL-terminated array of <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures to be deallocated.


## -returns



None.




## -remarks



Use this function only to free an array of 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures returned by <a href="https://msdn.microsoft.com/bca69428-27e1-4028-bfcd-ad67bee672cc">ber_scanf</a> with the <b>V</b> character included in the format string.

An application should not call this function to free a <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures that it has allocated.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>
 

 

