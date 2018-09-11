---
UID: NF:winber.ber_free
title: ber_free function
author: windows-sdk-content
description: The ber_free function frees a BerElement structure that was previously allocated with ber_alloc_t, ber_init, or the ldap_first_attribute/ ldap_next_attribute search functions.
old-location: ldap\ber_free.htm
tech.root: ldap
ms.assetid: b0f5a81e-a1d1-41c3-802c-b17be2275964
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ber_free, ber_free, ber_free function [LDAP], ldap.ber__free, ldap.ber_free, winber/ber_free"
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
 - ber_free
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ber_free function


## -description


The <b>ber_free</b> function frees a 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure that was previously allocated with 
<a href="https://msdn.microsoft.com/2a6fd54a-5ef7-49e3-98dd-da26bd98f89b">ber_alloc_t</a>, 
<a href="https://msdn.microsoft.com/ad6557e9-1683-4ffd-a59e-8f37eb67d089">ber_init</a>, or the 
<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>/
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a> search functions.


## -parameters




### -param pBerElement [in]

Pointer to the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure to be deallocated.


### -param fbuf [in]

Must be set to 0 if freeing structures allocated by 
<a href="https://msdn.microsoft.com/2a654ef4-519f-41a7-943e-3befe5c932e8">ldap_first_attribute</a>/
<a href="https://msdn.microsoft.com/4df50d80-0d01-4d7f-b542-865b84bac2a5">ldap_next_attribute</a>, otherwise it must be set to 1.


## -returns



None.




## -see-also




<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/2a6fd54a-5ef7-49e3-98dd-da26bd98f89b">ber_alloc_t</a>
 

 

