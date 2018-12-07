---
UID: NF:winldap.ldap_next_reference
title: ldap_next_reference function
author: windows-sdk-content
description: Retrieves a reference from a search result chain.
old-location: ldap\ldap_next_reference.htm
tech.root: ldap
ms.assetid: ea67f0e9-5cf7-4755-9bfd-856e26589a8d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_ldap_ldap_next_reference, ldap.ldap__next__reference, ldap.ldap_next_reference, ldap_next_reference, ldap_next_reference function [LDAP], winldap/ldap_next_reference"
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
 - ldap_next_reference
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_next_reference function


## -description


The <b>ldap_next_reference</b> function retrieves a reference from a search result chain.


## -parameters




### -param ld [in]

The session handle.


### -param entry [in]

The entry returned by a previous call to 
<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a> or <b>ldap_next_reference</b>.


## -returns



If the search returned valid results, this function returns a pointer to the next result entry in the results set. If no further entries or references exist in the result set, it returns <b>NULL</b>. This is the only error return; the session error parameter in the LDAP data structure is cleared to 0 in either case.




## -remarks



Use <b>ldap_next_reference</b> in conjunction with 
<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a> to step through and retrieve a list of continuation references from a search result chain.

The function returns subordinate referrals (references) that are returned in search responses. A subordinate referral is one in which the server has returned some data and the referral has been passed to other naming contexts below the current level in the tree. To step through external references in which the naming context does not reside on the server, use 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>.

You are not required to explicitly free the returned reference, as it is freed when the message itself is freed.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>



<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>
 

 

