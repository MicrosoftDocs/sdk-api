---
UID: NF:winldap.ldap_value_free_len
title: ldap_value_free_len function (winldap.h)
author: windows-sdk-content
description: The ldap_value_free_len frees berval structures that were returned by ldap_get_values_len.
old-location: ldap\ldap_value_free_len.htm
tech.root: ldap
ms.assetid: bae95e09-bb3b-4fb3-887f-3cff0a0e6c22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_ldap_ldap_value_free_len, ldap.ldap__value__free__len, ldap.ldap_value_free_len, ldap_value_free_len, ldap_value_free_len function [LDAP], winldap/ldap_value_free_len"
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
 - ldap_value_free_len
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_value_free_len function


## -description


The <b>ldap_value_free_len</b> frees 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-berval">berval</a> structures that were returned by 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a>.


## -parameters




### -param vals [in]

The structure to free.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.




## -remarks



Call <b>ldap_value_free_len</b> to free <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-berval">berval</a> structures returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-berval">berval</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a>
 

 

