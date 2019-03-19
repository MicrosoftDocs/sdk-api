---
UID: NF:winber.ber_bvdup
title: ber_bvdup function (winber.h)
author: windows-sdk-content
description: The ber_bvdup function creates a copy of the supplied berval structure.
old-location: ldap\ber_bvdup.htm
tech.root: ldap
ms.assetid: 512addea-2738-4063-970a-10c5c365fc7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ber_bvdup, ber_bvdup, ber_bvdup function [LDAP], ldap.ber__bvdup, ldap.ber_bvdup, winber/ber_bvdup"
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
 - ber_bvdup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ber_bvdup function


## -description


The <b>ber_bvdup</b> function creates a copy of the supplied 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure.


## -parameters




### -param pBerVal [in]

Pointer to the source <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure.


## -returns



If the function succeeds, the return value is a pointer to the newly allocated <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure.

If the function fails, it returns a <b>NULL</b> pointer.




## -remarks



The allocated <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> should be freed with <a href="https://msdn.microsoft.com/9e5a4bb9-568d-48ee-be75-952916c021b1">ber_bvfree</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>
 

 

