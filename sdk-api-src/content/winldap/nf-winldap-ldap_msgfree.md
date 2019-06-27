---
UID: NF:winldap.ldap_msgfree
title: ldap_msgfree function (winldap.h)
author: windows-sdk-content
description: The ldap_msgfree function frees the results obtained from a previous call to ldap_result, or to one of the synchronous search routines.
old-location: ldap\ldap_msgfree.htm
tech.root: ldap
ms.assetid: a4292638-0686-4c2d-8c51-1d5d079d5782
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_msgfree, ldap.ldap__msgfree, ldap.ldap_msgfree, ldap_msgfree, ldap_msgfree function [LDAP], winldap/ldap_msgfree"
ms.topic: function
f1_keywords: 
 - "winldap/ldap_msgfree"
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
 - ldap_msgfree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_msgfree function


## -description


The <b>ldap_msgfree</b> function frees the results obtained from a previous call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>, or to one of the synchronous search routines.


## -parameters




### -param res [in]

The result, or chain of results, to free.


## -returns



Returns <b>LDAP_SUCCESS</b>.




## -remarks



Call <b>ldap_msgfree</b> to free the result structure pointed to by the <i>res</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_s">ldap_search_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_st">ldap_search_st</a>
 

 

