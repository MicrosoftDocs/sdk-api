---
UID: NF:winldap.ldap_first_entry
title: ldap_first_entry function
author: windows-sdk-content
description: The ldap_first_entry function returns the first entry of a message.
old-location: ldap\ldap_first_entry.htm
old-project: ldap
ms.assetid: 1692d091-7963-492d-9998-5680a2a81088
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_first_entry, ldap.ldap__first__entry, ldap.ldap_first_entry, ldap_first_entry, ldap_first_entry function [LDAP], winldap/ldap_first_entry"
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
 - ldap_first_entry
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_first_entry function


## -description


The <b>ldap_first_entry</b> function returns the first entry of a message.


## -parameters




### -param ld [in]

The session handle.


### -param res [in]

The search result, as obtained by a call to one of the synchronous search routines or 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>.


## -returns



If the search returned valid results, this function returns a pointer to the first result entry. If no entry or reference exists in the result set, it returns <b>NULL</b>. This is the only error return; the session error parameter in the LDAP data structure is cleared to 0 in either case.




## -remarks



Use <b>ldap_first_entry</b> in conjunction with 
<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a> to step through and retrieve the list of entries from a search result chain.

You do not have to explicitly free the returned entry as it is freed when the message itself is freed.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/a0920107-6f99-4d28-a12f-c7f952933472">ldap_next_entry</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>
 

 

