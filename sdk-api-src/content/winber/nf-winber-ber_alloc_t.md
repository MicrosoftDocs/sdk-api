---
UID: NF:winber.ber_alloc_t
title: ber_alloc_t function (winber.h)
author: windows-sdk-content
description: Allocates and constructs a new BerElement structure.
old-location: ldap\ber_alloc_t.htm
tech.root: ldap
ms.assetid: 2a6fd54a-5ef7-49e3-98dd-da26bd98f89b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ber_alloc_t, ber_alloc_t, ber_alloc_t function [LDAP], ldap.ber__alloc__t, ldap.ber_alloc_t, winber/ber_alloc_t"
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
 - ber_alloc_t
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ber_alloc_t function


## -description


The <b>ber_alloc_t</b> function allocates and constructs a new 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


## -parameters




### -param options [in]

A bitwise OR of the options used to generate the encoding or decoding of the <b>BerElement</b>. The <b>LBER_USE_DER</b> flag (0x01) should always be specified, which causes the element lengths to be encoded in the minimum number of octets.

Unrecognized option bits are ignored.


## -returns



If the function succeeds, the return value is a pointer to the newly allocated <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.

If the function fails, it returns a <b>NULL</b> pointer.




## -remarks



The <b>LBER_USE_DER</b> option does not cause values of sets to be rearranged in tag and byte order or default values to be removed, so these functions are not sufficient for generating DER output as defined in X.509 and X.680. If the caller handles ordering values of sets correctly and removing default values, DER output as defined in X.509 and X.680 can be produced.

The allocated <b>BerElement</b> should be freed with <a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a>.




## -see-also




<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a>



<a href="https://msdn.microsoft.com/6bae449b-eb75-4598-aacc-65567de67997">ber_printf</a>
 

 

