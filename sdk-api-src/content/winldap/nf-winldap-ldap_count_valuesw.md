---
UID: NF:winldap.ldap_count_valuesW
title: ldap_count_valuesW function
author: windows-sdk-content
description: The ldap_count_values function counts the number of values in a list.
old-location: ldap\ldap_count_values.htm
tech.root: LDAP
ms.assetid: 3b00eeea-a966-4cf1-b945-2f052cae727a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "_ldap_ldap_count_values, ldap.ldap__count__values, ldap.ldap_count_values, ldap_count_values, ldap_count_values function [LDAP], ldap_count_valuesA, ldap_count_valuesW, winldap/ldap_count_values, winldap/ldap_count_valuesA, winldap/ldap_count_valuesW"
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
req.unicode-ansi: ldap_count_valuesW (Unicode) and ldap_count_valuesA (ANSI)
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
 - ldap_count_values
 - ldap_count_valuesA
 - ldap_count_valuesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ldap_count_valuesW
: 
---

# ldap_count_valuesW function


## -description


The <b>ldap_count_values</b> function counts the number of values in a list.


## -parameters




### -param vals [in]

An array of null-terminated strings (values) returned by 
<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>.


## -returns



This function returns the number of values in the array. There is no error return.

If a <b>NULL</b> pointer is passed as the argument, 0 is returned. If an invalid argument is passed, the value returned is undefined.




## -remarks



The <b>ldap_count_values</b> function returns the number of values in an array of strings. To count binary values in an array of 
<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a> structures, call 
<a href="https://msdn.microsoft.com/fab632c7-3ec6-4968-a48d-5865e7f43d0b">ldap_count_values_len</a>.




## -see-also




<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/844093e1-daba-494d-91b3-67455ff2e456">LDAP</a>



<a href="https://msdn.microsoft.com/38482501-faa1-4055-9758-e1e0a4199688">Searching a Directory</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>



<a href="https://msdn.microsoft.com/fab632c7-3ec6-4968-a48d-5865e7f43d0b">ldap_count_values_len</a>



<a href="https://msdn.microsoft.com/a633afa1-4a37-4894-ae94-5225d99077fd">ldap_get_values</a>
 

 

