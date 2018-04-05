---
UID: NF:winldap.ldap_search_abandon_page
title: ldap_search_abandon_page function
author: windows-driver-content
description: The ldap_search_abandon_page function terminates a paged-results search.
old-location: ldap\ldap_search_abandon_page.htm
old-project: LDAP
ms.assetid: 0c434611-b4d0-46e4-8e81-fc221e63de9f
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: "_ldap_ldap_search_abandon_page, ldap.ldap__search__abandon__page, ldap.ldap_search_abandon_page, ldap_search_abandon_page, ldap_search_abandon_page function [LDAP], winldap/ldap_search_abandon_page"
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
req.typenames: VOLUME_GET_GPT_ATTRIBUTES_INFORMATION, *PVOLUME_GET_GPT_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wldap32.dll
api_name:
-	ldap_search_abandon_page
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_search_abandon_page function


## -description


The <b>ldap_search_abandon_page</b> function terminates a paged-results search.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param SearchBlock [in]

A handle to the search block for the current search.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



Call <b>ldap_search_abandon_page</b> after a search has completed (when the server returns <b>LDAP_NO_RESULTS_RETURNED</b>) to perform necessary cleanup. You can also use this function to abandon a search at any time after the search block has been allocated.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>
 

 

