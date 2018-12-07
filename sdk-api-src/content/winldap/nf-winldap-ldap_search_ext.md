---
UID: NF:winldap.ldap_search_ext
title: ldap_search_ext function
author: windows-sdk-content
description: Searches the LDAP directory and returns a requested set of attributes for each matched entry.
old-location: ldap\ldap_search_ext.htm
tech.root: ldap
ms.assetid: 25ba88f3-44f6-42b8-9d33-6e57f2484738
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LDAP_SCOPE_BASE, LDAP_SCOPE_ONELEVEL, LDAP_SCOPE_SUBTREE, _ldap_ldap_search_ext, ldap.ldap__search__ext, ldap.ldap_search_ext, ldap_search_ext, ldap_search_ext function [LDAP], ldap_search_extA, ldap_search_extW, winldap/ldap_search_ext, winldap/ldap_search_extA, winldap/ldap_search_extW
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
req.unicode-ansi: ldap_search_extW (Unicode) and ldap_search_extA (ANSI)
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
 - ldap_search_ext
 - ldap_search_extA
 - ldap_search_extW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_search_ext function


## -description


The <b>ldap_search_ext</b> function searches the LDAP directory and returns a requested set of attributes for each matched entry.


## -parameters




### -param ld [in]

The session handle.


### -param base [in]

A pointer to a null-terminated string that contains the distinguished name of the entry at which to start the search.


### -param scope [in]

Specifies one of the following values to indicate the search scope.



#### LDAP_SCOPE_BASE

Search the base entry only.



#### LDAP_SCOPE_ONELEVEL

Search all entries in the first level below the base entry, excluding the base entry.



#### LDAP_SCOPE_SUBTREE

Search the base entry and all entries in the tree below the base.


### -param filter [in]

A pointer to a null-terminated string that specifies the search filter. For more information, see 
<a href="https://msdn.microsoft.com/3ce4709c-5ef7-4713-8fb7-b46ab284339f">Search Filter Syntax</a>.


### -param attrs [in]

A null-terminated array of null-terminated strings that indicate which attributes to return for each matching entry. To retrieve all available attributes, pass <b>NULL</b>.


### -param attrsonly [in]

A Boolean value that should be zero if both attribute types and values are to be returned, nonzero if only types are to be returned.


### -param ServerControls [in]

A list of LDAP server controls.


### -param ClientControls [in]

A list of client controls.


### -param TimeLimit [in]

Specifies both the local search time-out value in seconds and the operation time limit sent to the server within the search request.


### -param SizeLimit [in]

A limit on the number of entries to return from the search. A value of zero indicates no limit.


### -param MessageNumber [out]

The request  message ID.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



The <b>ldap_search_ext</b> function initiates an asynchronous search operation. The parameters and effects of <b>ldap_search_ext</b> include those of 
<a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a>. The extended function includes additional parameters to support client and server controls and thread safety, and to specify size and time limits for each search operation.

Use the 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a> function with the <i>ld</i> session handle to set the <b>LDAP_OPT_DEREF</b> option that determine how the search is performed. For more information, see 
<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>. Two other session options, <b>LDAP_OPT_SIZELIMIT</b> and <b>LDAP_OPT_TIMELIMIT</b>, are ignored in favor of the <i>SizeLimit</i> and <i>TimeLimit</i> parameters in this function.

If the operation succeeds, <b>ldap_search_ext</b> passes the message ID to the caller as a parameter when the operation returns successfully. Call 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a> with the message ID to get the result of the operation.

An LDAP client application that must control the rate at which results are returned may specify the search request to provide a paged results control with size set to the desired page size and cookie set to the zero-length string. The page size specified may be greater than zero and less than the <i>SizeLimit</i> value specified in the search request.

If the page size is greater than or equal to the <i>SizeLimit</i> value option described in 
<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>, the server should ignore the control because the request can be satisfied in a single page. If the server does not support this control, the server must return an error of unsupported Critical Extension if the client requested it as critical, otherwise the server should ignore the control. The remainder of this section assumes the server does not ignore the client's paged results control.

The client sends the server a search request with the simple paged results control, along with an empty previous enumeration key, also known as a "cookie," and the initial page size. The server then returns the number of entries specified by the page size and also returns a cookie issued on the next client request to get the next page of results. The client then issues a search, with the cookie included, optionally resetting the page size. The server then responds by returning the results, up to the specified number of entries. To instruct the function to return the results directly, use the synchronous routine 
<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>.

Multithreading: Calls to <b>ldap_search_ext</b> are thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa772153(v=VS.85).aspx">Change Notifications in Active Directory</a>



<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/fe0d782b-8faf-4666-a952-e2bfd33f6d67">ldap_search</a>



<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>
 

 

