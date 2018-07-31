---
UID: NF:winldap.ldap_get_optionW
title: ldap_get_optionW function
author: windows-sdk-content
description: Retrieves the current values of session-wide parameters.
old-location: ldap\ldap_get_option.htm
old-project: LDAP
ms.assetid: e07c2c3d-8099-4f9c-9ee7-26c1287110d5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "_ldap_ldap_get_option, ldap.ldap__get__option, ldap.ldap_get_option, ldap_get_option, ldap_get_option function [LDAP], ldap_get_optionW, winldap/ldap_get_option, winldap/ldap_get_optionW"
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
req.unicode-ansi: ldap_get_optionW (Unicode) and ldap_get_option (ANSI)
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
 - ldap_get_option
 - ldap_get_option
 - ldap_get_optionW
product: Windows
targetos: Windows
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ldap_get_optionW function


## -description


The <b>ldap_get_option</b> function retrieves the current values of session-wide parameters.


## -parameters




### -param ld [in]

The session handle.


### -param option [in]

The name of the option accessed. For more information and  a list of allowable options and their values, see the following Remarks section.


### -param outvalue [out]

The address of the option value. The actual type of this parameter depends on the setting of the option parameter.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>.




## -remarks



For more information and a description of optional settings that apply to an LDAP session, see 
<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>. The <i>outvalue</i> value returns a pointer to an allocated block of memory of the type listed in the <b>Session Options</b> table; this memory should be freed using <a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a> when the data is no longer required, unless it is explicitly mentioned in the <b>Session Options</b> table not to free the returned memory.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">LDAP_OPT_ERROR_STRING</a> returns a pointer to an internal static string table, and <a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a> should not be called when using this session option.</div>
<div> </div>
Multithreading: The <b>ldap_get_option</b> function is thread-safe.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/1447d242-b8db-4b7e-9871-2193f747be4e">Getting and Setting Session Options</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/a968e66d-933f-44b7-b74d-d18a92d7de3f">Session Options</a>



<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>



<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>
 

 

