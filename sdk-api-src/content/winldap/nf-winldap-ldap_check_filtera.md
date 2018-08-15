---
UID: NF:winldap.ldap_check_filterA
title: ldap_check_filterA function
author: windows-sdk-content
description: The ldap_check_filter function is used to verify filter syntax.
old-location: ldap\ldap_check_filter.htm
old-project: ldap
ms.assetid: 33b549bc-4b23-484a-a7cf-f4963154d492
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_check_filter, ldap.ldap__check__filter, ldap.ldap_check_filter, ldap_check_filter, ldap_check_filter function [LDAP], ldap_check_filterA, ldap_check_filterW, winldap/ldap_check_filter, winldap/ldap_check_filterA, winldap/ldap_check_filterW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winldap.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_check_filterW (Unicode) and ldap_check_filterA (ANSI)
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
 - ldap_check_filter
 - ldap_check_filterA
 - ldap_check_filterW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_check_filterA function


## -description


The <b>ldap_check_filter</b> function is used to verify filter syntax.


## -parameters




### -param ld [in]

The session handle.


### -param SearchFilter [in]

A pointer to a wide, null-terminated string that contains the name of the filter to check.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



Use <b>ldap_check_filter</b> to verify the syntax of a search filter before initiating a search. This syntax check does not perform a full verification of the search filter syntax against RFC 2254 rules. Rather, it verifies that the filter meets the minimum syntactic requirements for encoding required by the wldap32 search-filter-encoding routines. As a result, a search filter can pass an <b>ldap_check_filter</b> operation, and can be encoded by wldap32, but the server may still detect a RFC 2254 compliance violation and reject the search filter.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a>
 

 

