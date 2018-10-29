---
UID: NF:winldap.ldap_modify_extA
title: ldap_modify_extA function
author: windows-sdk-content
description: The ldap_modify_ext function changes an existing entry.
old-location: ldap\ldap_modify_ext.htm
tech.root: LDAP
ms.assetid: a11f4944-d574-4215-a25e-536adf21c469
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_ldap_ldap_modify_ext, ldap.ldap__modify__ext, ldap.ldap_modify_ext, ldap_modify_ext, ldap_modify_ext function [LDAP], ldap_modify_extA, ldap_modify_extW, winldap/ldap_modify_ext, winldap/ldap_modify_extA, winldap/ldap_modify_extW"
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
req.unicode-ansi: ldap_modify_extW (Unicode) and ldap_modify_extA (ANSI)
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
 - ldap_modify_ext
 - ldap_modify_extA
 - ldap_modify_extW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_modify_extA function


## -description


The <b>ldap_modify_ext</b> function changes an existing entry.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the name of the entry to modify.


### -param mods [in]

A null-terminated array of modifications to make to the entry.


### -param ServerControls [in]

A list of LDAP server controls.


### -param ClientControls [in]

A list of client controls


### -param MessageNumber [out]

This result parameter is set to the message ID of the request if the call succeeds.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_modify_ext</b> function initiates an asynchronous operation to modify an existing entry. If values are being added or replaced in the entry, the function creates the attribute, if necessary. If values are being deleted, and no values remain, the function removes the attribute. All modifications are performed in the order in which they are listed.

The parameters and effects of <b>ldap_modify_ext</b> subsume those of 
<a href="https://msdn.microsoft.com/93ae0af4-1b16-4bb0-952f-139241189d79">ldap_modify</a>. The extended routine includes additional parameters to support client and server controls, and thread safety.

If successful, <b>ldap_modify_ext</b> passes back the message ID for the operation in the <i>MessageNumber</i> parameter. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to obtain the result of the operation. If you prefer to have the function return the result directly, use the synchronous extended function 
<a href="https://msdn.microsoft.com/d71190d6-4775-4f37-b509-3395a7352272">ldap_modify_ext_s</a>.

Multithreading: Calls to <b>ldap_modify_ext</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/93ae0af4-1b16-4bb0-952f-139241189d79">ldap_modify</a>



<a href="https://msdn.microsoft.com/d71190d6-4775-4f37-b509-3395a7352272">ldap_modify_ext_s</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

