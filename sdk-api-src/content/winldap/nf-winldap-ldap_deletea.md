---
UID: NF:winldap.ldap_deleteA
title: ldap_deleteA function
author: windows-sdk-content
description: The ldap_delete function deletes an entry from the directory tree.
old-location: ldap\ldap_delete.htm
old-project: LDAP
ms.assetid: 314f3128-ab09-45a7-a678-779d5b7d4d72
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_delete, ldap.ldap__delete, ldap.ldap_delete, ldap_delete, ldap_delete function [LDAP], ldap_deleteA, ldap_deleteW, winldap/ldap_delete, winldap/ldap_deleteA, winldap/ldap_deleteW"
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
req.unicode-ansi: ldap_deleteW (Unicode) and ldap_deleteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_delete
-	ldap_deleteA
-	ldap_deleteW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_deleteA function


## -description


The <b>ldap_delete</b> function deletes an entry from the directory tree.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.


## -returns



If the function succeeds, it returns the message ID of the delete operation.

If the function fails, the return value is –1 and the function sets the session error parameters in the 
<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a> data structure. To retrieve this value, use <a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a>.




## -remarks



Call <b>ldap_delete</b> to remove a leaf entry from the directory tree. Be aware that LDAP does not support deletion of entire subtrees in a single operation. As an asynchronous function, <b>ldap_delete</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous delete operation before it has completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

To have the function return the results directly, use the synchronous routine 
<a href="https://msdn.microsoft.com/cded1b76-0fad-454f-bf5a-c500c9079f08">ldap_delete_s</a>. Use 
<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a> or 
<a href="https://msdn.microsoft.com/eb00a5c1-b7b8-4b68-9d91-d52235f5e1ff">ldap_delete_ext_s</a> to enable support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_delete</b> are thread-safe, provided that 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting any other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/65c4fa7c-76d8-47ec-b5c5-bf671529f5f1">ldap_delete_ext</a>



<a href="https://msdn.microsoft.com/eb00a5c1-b7b8-4b68-9d91-d52235f5e1ff">ldap_delete_ext_s</a>



<a href="https://msdn.microsoft.com/cded1b76-0fad-454f-bf5a-c500c9079f08">ldap_delete_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 

