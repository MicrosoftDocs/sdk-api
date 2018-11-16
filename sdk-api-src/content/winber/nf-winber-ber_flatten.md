---
UID: NF:winber.ber_flatten
title: ber_flatten function
author: windows-sdk-content
description: The ber_flatten function allocates a new berval structure containing the data taken from the supplied BerElement structure.
old-location: ldap\ber_flatten.htm
tech.root: LDAP
ms.assetid: c253100b-092e-4975-8411-31edb7791068
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_ldap_ber_flatten, ber_flatten, ber_flatten function [LDAP], ldap.ber__flatten, ldap.ber_flatten, winber/ber_flatten"
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
 - ber_flatten
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ber_flatten
: 
---

# ber_flatten function


## -description


The <b>ber_flatten</b> function allocates a new 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure containing the data taken from the supplied 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


## -parameters




### -param pBerElement [in]

Pointer to the source <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param pBerVal [out]

Pointer to the newly allocated <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structure, which should be freed using 
<a href="https://msdn.microsoft.com/9e5a4bb9-568d-48ee-be75-952916c021b1">ber_bvfree</a>.


## -returns



The function returns 0 on success and -1 on failure.




## -remarks



The use of <b>ber_flatten</b> on a <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> in which all <b>{</b> and <b>}</b> format modifiers have not been properly matched will cause the function to return an error.




## -see-also




<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/9e5a4bb9-568d-48ee-be75-952916c021b1">ber_bvfree</a>



<a href="https://msdn.microsoft.com/ad6557e9-1683-4ffd-a59e-8f37eb67d089">ber_init</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>
 

 

