---
UID: NF:winldap.ldap_value_free_len
title: ldap_value_free_len function (winldap.h)
author: windows-sdk-content
description: The ldap_value_free_len frees berval structures that were returned by ldap_get_values_len.
old-location: ldap\ldap_value_free_len.htm
tech.root: ldap
ms.assetid: bae95e09-bb3b-4fb3-887f-3cff0a0e6c22
ms.author: windowssdkdev
ms.date: 12/5/2018
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
---

# ldap_value_free_len function


## -description


The <b>ldap_value_free_len</b> frees 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures that were returned by 
<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>.


## -parameters




### -param vals [in]

The structure to free.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a> for more information.




## -remarks



Call <b>ldap_value_free_len</b> to free <a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures returned by <a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/822411b7-fc49-4b93-8e54-353350ed5de9">Return Values</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>



<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>
 

 

