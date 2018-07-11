---
UID: NF:winldap.ldap_modify_sA
title: ldap_modify_sA function
author: windows-sdk-content
description: The ldap_modify_s function changes an existing entry.
old-location: ldap\ldap_modify_s.htm
old-project: ldap
ms.assetid: 26002d58-a4ac-4fd6-aa63-39210f8fc883
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: "_ldap_ldap_modify_s, ldap.ldap__modify__s, ldap.ldap_modify_s, ldap_modify_s, ldap_modify_s function [LDAP], ldap_modify_sA, ldap_modify_sW, winldap/ldap_modify_s, winldap/ldap_modify_sA, winldap/ldap_modify_sW"
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
req.unicode-ansi: ldap_modify_sW (Unicode) and ldap_modify_sA (ANSI)
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
 - ldap_modify_s
 - ldap_modify_sA
 - ldap_modify_sW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_modify_sA function


## -description


The <b>ldap_modify_s</b> function changes an existing entry.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the name of the entry to modify.


### -param mods [in]

A null-terminated array of modifications to make to the entry.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



The <b>ldap_modify_s</b> function initiates a synchronous operation to modify an existing entry. If values are being added to or replaced in the entry, the function creates the attribute, if necessary. If values are being deleted, the function removes the attribute if no values remain. All modifications are performed in the order in which they are listed.

Multithreading: Calls to <b>ldap_modify_s</b> are thread-safe.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation (by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines) before attempting any other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/07761668-e0d9-4ab0-b8ce-ce8626389e03">LDAPMod</a>



<a href="https://msdn.microsoft.com/ad7be3a1-663c-489e-8eb3-1aea910ee366">Modifying a Directory Entry</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/93ae0af4-1b16-4bb0-952f-139241189d79">ldap_modify</a>



<a href="https://msdn.microsoft.com/a11f4944-d574-4215-a25e-536adf21c469">ldap_modify_ext</a>



<a href="https://msdn.microsoft.com/d71190d6-4775-4f37-b509-3395a7352272">ldap_modify_ext_s</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 

