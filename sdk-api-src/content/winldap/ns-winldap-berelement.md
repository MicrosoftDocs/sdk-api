---
UID: NS:winldap.berelement
title: BerElement (winldap.h)
author: windows-sdk-content
description: C++ class object that performs basic encoding rules (BER) encoding.
old-location: ldap\berelement.htm
tech.root: ldap
ms.assetid: 491bdf54-0b45-4324-93fc-35fe15155a3d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BerElement, BerElement structure [LDAP], _ldap_berelement, ldap.berelement, winldap/BerElement
ms.topic: struct
req.header: winldap.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - BerElement
product: Windows
targetos: Windows
req.typenames: BerElement
req.redist: 
---

# BerElement structure


## -description


A <b>BerElement</b> structure is a C++ class object that performs basic encoding rules (BER) encoding.


## -struct-fields




### -field opaque

Pointer to an opaque buffer. Do not attempt to access it.


## -remarks



This is an opaque data structure that the 
 <a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a> function allocates and returns to indicate the current position during a traversal of an attribute list. Pass the pointer to this structure to the 
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a> function.

<div class="alert"><b>Caution</b>  When allocated by one of the two previous functions, you do not free the memory associated with this structure or its pointer when the <b>BerElement</b> is no longer required.</div>
<div> </div>
A <b>BerElement</b> structure can also be allocated by calling the <a href="https://msdn.microsoft.com/2a6fd54a-5ef7-49e3-98dd-da26bd98f89b">ber_alloc_t</a> or the <a href="https://msdn.microsoft.com/ad6557e9-1683-4ffd-a59e-8f37eb67d089">ber_init</a> function. In such cases, free the   memory allocated to the <b>BerElement</b> structure by using the <a href="https://msdn.microsoft.com/b0f5a81e-a1d1-41c3-802c-b17be2275964">ber_free</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>



<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>
 

 

