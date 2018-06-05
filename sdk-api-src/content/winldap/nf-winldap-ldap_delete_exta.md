---
UID: NF:winldap.ldap_delete_extA
title: ldap_delete_extA function
author: windows-sdk-content
description: The ldap_delete_ext function is an extended routine that removes a leaf entry from the directory tree.
old-location: ldap\ldap_delete_ext.htm
old-project: LDAP
ms.assetid: 65c4fa7c-76d8-47ec-b5c5-bf671529f5f1
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: "_ldap_ldap_delete_ext, ldap.ldap__delete__ext, ldap.ldap_delete_ext, ldap_delete_ext, ldap_delete_ext function [LDAP], ldap_delete_extA, ldap_delete_extW, winldap/ldap_delete_ext, winldap/ldap_delete_extA, winldap/ldap_delete_extW"
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
req.unicode-ansi: ldap_delete_extW (Unicode) and ldap_delete_extA (ANSI)
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
-	ldap_delete_ext
-	ldap_delete_extA
-	ldap_delete_extW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_delete_extA function


## -description


The <b>ldap_delete_ext</b> function is an extended routine that removes a leaf entry from the directory tree.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to delete.


### -param ServerControls [in]

Optional. List of LDAP server controls. If not used, set this parameter to NULL.


### -param ClientControls [in]

Optional. List of client controls. If not used, set this parameter to <b>NULL</b>.


### -param MessageNumber [out]

Message ID for the request.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_delete_ext</b> function removes a leaf entry from the directory tree. LDAP does not support deletion of entire subtrees in a single operation, however there is an extended control, <a href="https://msdn.microsoft.com/b47a0f40-7191-40a5-a914-6c4fa78df8cb">LDAP_SERVER_TREE_DELETE_OID</a>, used to perform this operation.

The parameters and effects of <b>ldap_delete_ext</b> include those of 
<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a>. The extended routine includes parameters to support client and server controls and thread safety.

If the operation succeeds, <b>ldap_delete_ext</b> passes the message ID to the caller as a parameter when the operation returns successfully. To get the result of the operation, call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID.

To have the function return the results directly, use the synchronous routine 
<a href="https://msdn.microsoft.com/eb00a5c1-b7b8-4b68-9d91-d52235f5e1ff">ldap_delete_ext_s</a>.

Multithreading: Calls to <b>ldap_delete_ext</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/314f3128-ab09-45a7-a678-779d5b7d4d72">ldap_delete</a>



<a href="https://msdn.microsoft.com/eb00a5c1-b7b8-4b68-9d91-d52235f5e1ff">ldap_delete_ext_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

