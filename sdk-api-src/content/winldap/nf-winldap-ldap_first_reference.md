---
UID: NF:winldap.ldap_first_reference
title: ldap_first_reference function
author: windows-sdk-content
description: Returns the first reference from a message.
old-location: ldap\ldap_first_reference.htm
old-project: LDAP
ms.assetid: b9ee4da3-9309-4e2b-95a9-6e0f1625fc79
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "_ldap_ldap_first_reference, ldap.ldap__first__reference, ldap.ldap_first_reference, ldap_first_reference, ldap_first_reference function [LDAP], winldap/ldap_first_reference"
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
req.unicode-ansi: 
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
 - ldap_first_reference
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_first_reference function


## -description


The <b>ldap_first_reference</b> function returns the first reference from a message.


## -parameters




### -param ld [in]

The session handle.


### -param res [in]

The search result, as obtained by a call to one of the synchronous search routines or 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.


## -returns



If the search returned valid results, this function returns a pointer to the first result reference. If no entry or reference exists in the result set, it returns <b>NULL</b>. This is the only error return; the session error parameter in the LDAP data structure is cleared to 0 in either case.




## -remarks



Use <b>ldap_first_reference</b> in conjunction with 
<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a> to step through and retrieve a list of continuation references from a search result chain.

The function returns subordinate referrals (references) that are returned in search responses. A subordinate referral is one in which the server has returned some data and the referral has been passed to other naming contexts below the current level in the tree. To step through external references in which the naming context does not reside on the server, use 
<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a> instead.

You do not have to explicitly free the returned reference as it is freed when the message itself is freed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>



<a href="https://msdn.microsoft.com/6cadfbe0-0b69-4c43-a2ca-d8b3a12bf0a9">ldap_parse_result</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

