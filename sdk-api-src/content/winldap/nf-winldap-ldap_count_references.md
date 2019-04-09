---
UID: NF:winldap.ldap_count_references
title: ldap_count_references function (winldap.h)
author: windows-sdk-content
description: The ldap_count_references function counts the number of subordinate references that were returned by the server in a response to a search request.
old-location: ldap\ldap_count_references.htm
tech.root: ldap
ms.assetid: 1d216f39-6eb4-4c3d-8f97-92835aac2aca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_count_references, ldap.ldap__count__references, ldap.ldap_count_references, ldap_count_references, ldap_count_references function [LDAP], winldap/ldap_count_references"
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
 - ldap_count_references
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_count_references function


## -description


The <b>ldap_count_references</b> function counts the number of subordinate references that were returned by the server in a response to a search request.


## -parameters




### -param ld [in]

The session handle.


### -param res [in]

The search result obtained by a call to one of the synchronous search routines or to 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.


## -returns



If the function succeeds, it returns the number of references.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.




## -remarks



The <b>ldap_count_references</b> function returns the number of references contained in a chain of search results. It can also be used to count the number of references that remain in a chain. Call the function with the return value from 
<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>, 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>, 
<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>, 
<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>, or 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/6e53b914-2ad8-408a-9671-50a01a8a42f1">ldap_count_entries</a>



<a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a>



<a href="https://msdn.microsoft.com/1692d091-7963-492d-9998-5680a2a81088">ldap_first_entry</a>



<a href="https://msdn.microsoft.com/b9ee4da3-9309-4e2b-95a9-6e0f1625fc79">ldap_first_reference</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/ea67f0e9-5cf7-4755-9bfd-856e26589a8d">ldap_next_reference</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

