---
UID: NF:winldap.ldap_msgfree
title: ldap_msgfree function
author: windows-sdk-content
description: The ldap_msgfree function frees the results obtained from a previous call to ldap_result, or to one of the synchronous search routines.
old-location: ldap\ldap_msgfree.htm
tech.root: LDAP
ms.assetid: a4292638-0686-4c2d-8c51-1d5d079d5782
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "_ldap_ldap_msgfree, ldap.ldap__msgfree, ldap.ldap_msgfree, ldap_msgfree, ldap_msgfree function [LDAP], winldap/ldap_msgfree"
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
 - ldap_msgfree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_msgfree function


## -description


The <b>ldap_msgfree</b> function frees the results obtained from a previous call to 
<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>, or to one of the synchronous search routines.


## -parameters




### -param res [in]

The result, or chain of results, to free.


## -returns



Returns <b>LDAP_SUCCESS</b>.




## -remarks



Call <b>ldap_msgfree</b> to free the result structure pointed to by the <i>res</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/e047fccc-a875-4360-be1b-3ac3dea15dd6">ldap_result</a>



<a href="https://msdn.microsoft.com/7ce74c35-7a30-4757-a4f7-d5cd4a389584">ldap_search_ext_s</a>



<a href="https://msdn.microsoft.com/ed0a2c43-c38f-4991-b652-a1df4f739478">ldap_search_s</a>



<a href="https://msdn.microsoft.com/af2ab469-fa72-4a57-912c-42d9a6721806">ldap_search_st</a>
 

 

