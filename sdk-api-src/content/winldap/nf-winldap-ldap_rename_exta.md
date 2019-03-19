---
UID: NF:winldap.ldap_rename_extA
title: ldap_rename_extA function (winldap.h)
author: windows-sdk-content
description: The ldap_rename_ext function starts an asynchronous operation that changes the distinguished name of an entry in the directory. This function is available effective with LDAP 3.
old-location: ldap\ldap_rename_ext.htm
tech.root: ldap
ms.assetid: 73633a71-ebe6-4169-a9ff-17151d90ebcd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_rename_ext, ldap.ldap__rename__ext, ldap.ldap_rename_ext, ldap_rename_ext, ldap_rename_ext function [LDAP], ldap_rename_extA, ldap_rename_extW, winldap/ldap_rename_ext, winldap/ldap_rename_extA, winldap/ldap_rename_extW"
ms.topic: function
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_rename_extW (Unicode) and ldap_rename_extA (ANSI)
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
 - ldap_rename_ext
 - ldap_rename_extA
 - ldap_rename_extW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_rename_extA function


## -description


The <b>ldap_rename_ext</b> function starts an asynchronous operation that changes the distinguished name of an entry in the directory. This function is available effective with LDAP 3.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a wide, null-terminated string that contains the distinguished name of the entry to be renamed.


### -param NewRDN [in]

A pointer to a wide, null-terminated string that contains the new relative distinguished name for the entry.


### -param NewParent [in]

A pointer to a wide, null-terminated string that contains the distinguished name of the new parent for this entry. This parameter enables you to move the entry to a new parent container.


### -param DeleteOldRdn [in]

<b>TRUE</b> if the old relative distinguished name should be deleted; <b>FALSE</b> if the old relative distinguished name should be retained.


### -param ServerControls [in]

List of LDAP server controls.


### -param ClientControls [in]

List of client controls.


### -param MessageNumber [out]

Pointer to a variable that receives the message identifier for this asynchronous operation. Use this identifier with the 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> function to retrieve the results of the operation.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



This function provides extended renaming operations. For example, you can pass controls that separate the parent from the relative distinguished name, for clarity.

Multithreading: Calls to <b>ldap_rename_ext</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>
 

 

