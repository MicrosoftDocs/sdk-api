---
UID: NF:winldap.ldap_delete_s
title: ldap_delete_s function
author: windows-sdk-content
description: The ldap_delete_s function is a synchronous operation that removes a leaf entry from the directory tree.
old-location: ldap\ldap_delete_s.htm
old-project: ldap
ms.assetid: cded1b76-0fad-454f-bf5a-c500c9079f08
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_delete_s, ldap.ldap__delete__s, ldap.ldap_delete_s, ldap_delete_s, ldap_delete_s function [LDAP], ldap_delete_sA, ldap_delete_sW, winldap/ldap_delete_s, winldap/ldap_delete_sA, winldap/ldap_delete_sW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_delete_sW (Unicode) and ldap_delete_sA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_delete_s
 - ldap_delete_sA
 - ldap_delete_sW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_delete_s function


## -description


The <b>ldap_delete_s</b> function is a synchronous operation that removes a leaf entry from the directory tree.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Call <b>ldap_delete_s</b> to remove a leaf entry from the directory tree. Be aware that LDAP does not support deletion of entire subtrees in a single operation. As a synchronous operation, <b>ldap_delete_s</b> does not return until the operation is compete. Use 
<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a> or 
<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a> to perform the delete operation asynchronously.

Multithreading: The <b>ldap_delete_s</b> function is thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting any other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a>



<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 

