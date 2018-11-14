---
UID: NF:winldap.ldap_memfreeW
title: ldap_memfreeW function
author: windows-sdk-content
description: Frees memory allocated from the LDAP heap.
old-location: ldap\ldap_memfree.htm
tech.root: ldap
ms.assetid: 3256a202-4245-4bea-a66c-0f28bfe2ef7e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_ldap_ldap_memfree, ldap.ldap__memfree, ldap.ldap_memfree, ldap_memfree, ldap_memfree function [LDAP], ldap_memfreeA, ldap_memfreeW, winldap/ldap_memfree, winldap/ldap_memfreeA, winldap/ldap_memfreeW"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_memfreeW (Unicode) and ldap_memfreeA (ANSI)
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
 - ldap_memfree
 - ldap_memfreeA
 - ldap_memfreeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_memfreeW
: 
---

# ldap_memfreeW function


## -description


The <b>ldap_memfree</b> function frees memory allocated from the LDAP heap.


## -parameters




### -param Block [in]

A pointer to a null-terminated string that contains a pointer to memory allocated by the LDAP library.


## -returns



None.




## -remarks



Call <b>ldap_memfree</b> to free strings, such as the attribute names returned by <b>ldap_*_attribute</b>, or distinguished names returned by 
<a href="https://msdn.microsoft.com/00484fe7-65d2-4300-ab5c-0a69a25e65e6">ldap_get_dn</a>. Do not free the static buffers used by 
<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>, 
<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>, and others.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/00484fe7-65d2-4300-ab5c-0a69a25e65e6">ldap_get_dn</a>



<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>



<a href="https://msdn.microsoft.com/ebd7303d-e98d-454d-9964-d774d5c2a756">ldap_open</a>
 

 

