---
UID: NF:winldap.ldap_searchW
title: ldap_searchW function
author: windows-sdk-content
description: Searches the LDAP directory and returns a requested set of attributes for each matched entry.
old-location: ldap\ldap_search.htm
tech.root: LDAP
ms.assetid: fe0d782b-8faf-4666-a952-e2bfd33f6d67
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: LDAP_SCOPE_BASE, LDAP_SCOPE_ONELEVEL, LDAP_SCOPE_SUBTREE, _ldap_ldap_search, ldap.ldap__search, ldap.ldap_search, ldap_search, ldap_search function [LDAP], ldap_searchA, ldap_searchW, winldap/ldap_search, winldap/ldap_searchA, winldap/ldap_searchW
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
req.unicode-ansi: ldap_searchW (Unicode) and ldap_searchA (ANSI)
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
 - ldap_search
 - ldap_searchA
 - ldap_searchW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_searchW function


## -description


The <b>ldap_search</b> function searches the LDAP directory and returns a requested set of attributes for each matched entry.


## -parameters




### -param ld [in]

A session handle.


### -param base [in]

A pointer to a null-terminated string that contains the distinguished name of the entry at which to start the search.


### -param scope [in]

A data type that specifies one of the following values to indicate the search scope.



#### LDAP_SCOPE_BASE

Search only the base entry.



#### LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.



#### LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.


### -param filter [in]

A pointer to a null-terminated string that specifies the search filter. For more information, see 
<a href="https://msdn.microsoft.com/3ce4709c-5ef7-4713-8fb7-b46ab284339f">Search Filter Syntax</a>.


### -param attrs [in]

A null-terminated array of null-terminated strings that indicate which attributes to return for each matching entry. Pass <b>NULL</b> to retrieve available attributes.


### -param attrsonly [in]

Boolean value that should be zero if both attribute types and values are to be returned, nonzero if only types are required.


##### - scope.LDAP_SCOPE_BASE

Search only the base entry.


##### - scope.LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.


##### - scope.LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.


## -returns



If the function succeeds, it returns the message ID of the search operation.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.




## -remarks



The <b>ldap_search</b> function initiates an asynchronous search operation.

Use the 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a> function with the <i>ld</i> session handle to set the LDAP_OPT_SIZELIMIT, LDAP_OPT_TIMELIMIT, and LDAP_OPT_DEREF options that determine how the search is performed. For more information, see 
<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>.

As an asynchronous function, <b>ldap_search</b> returns a message ID for the operation. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous search operation before it has completed, call 
<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>.

To have the function return the results directly, use the synchronous routine 
<a href="https://msdn.microsoft.com/ed0a2c43-c38f-4991-b652-a1df4f739478">ldap_search_s</a>. Use 
<a href="https://msdn.microsoft.com/25ba88f3-44f6-42b8-9d33-6e57f2484738">ldap_search_ext</a> or 
<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a> to implement support for LDAP 3 server and client controls.

Multithreading: Calls to <b>ldap_search</b> are thread-safe, provided that 
<a href="https://msdn.microsoft.com/04bcdd90-344a-4f2d-a700-e725584e49d9">LdapGetLastError</a> is used to retrieve the actual session error code when the function call returns the -1 failure code.

<div class="alert"><b>Note</b>  When connecting to an LDAP 2 server, the application must perform a bind operation, by calling one of the 
<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a> or 
<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a> routines, before attempting other operations.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/5c238d98-77f5-4702-bae1-80cdec70a30c">ldap_abandon</a>



<a href="https://msdn.microsoft.com/889636f2-3dd0-4027-aa35-d7b7930d9e69">ldap_bind</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/25ba88f3-44f6-42b8-9d33-6e57f2484738">ldap_search_ext</a>



<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>



<a href="https://msdn.microsoft.com/ed0a2c43-c38f-4991-b652-a1df4f739478">ldap_search_s</a>



<a href="https://msdn.microsoft.com/13fc47c5-094b-4a91-8e5f-bfff8c72b431">ldap_simple_bind</a>
 

 

