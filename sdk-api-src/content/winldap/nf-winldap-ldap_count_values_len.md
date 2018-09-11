---
UID: NF:winldap.ldap_count_values_len
title: ldap_count_values_len function
author: windows-sdk-content
description: Counts the number of values in a list.
old-location: ldap\ldap_count_values_len.htm
tech.root: ldap
ms.assetid: fab632c7-3ec6-4968-a48d-5865e7f43d0b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "_ldap_ldap_count_values_len, ldap.ldap__count__values__len, ldap.ldap_count_values_len, ldap_count_values_len, ldap_count_values_len function [LDAP], winldap/ldap_count_values_len"
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
 - ldap_count_values_len
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ldap_count_values_len function


## -description


The <b>ldap_count_values_len</b> function counts the number of values in a list.


## -parameters




### -param vals [in]

An array of values returned by 
<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>.


## -returns



This function returns the number of values in the array. There is no error return.

If a <b>NULL</b> pointer is passed as the argument, 0 is returned. If an invalid argument is passed, the value returned is undefined.




## -remarks



The <b>ldap_count_values_len</b> function returns the number of binary values in an array of 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures. To count the values in an array of null-terminated character strings, call 
<a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>



<a href="https://msdn.microsoft.com/3b00eeea-a966-4cf1-b945-2f052cae727a">ldap_count_values</a>



<a href="https://msdn.microsoft.com/e2100892-5dad-4fc7-8129-34c675bcf134">ldap_get_values_len</a>
 

 

