---
UID: NF:winldap.ldap_count_valuesW
title: ldap_count_valuesW function (winldap.h)
description: The ldap_count_valuesW (Unicode) function (winldap.h) counts the number of values in a list.
helpviewer_keywords: ["_ldap_ldap_count_values", "ldap.ldap__count__values", "ldap.ldap_count_values", "ldap_count_values", "ldap_count_values function [LDAP]", "ldap_count_valuesW", "winldap/ldap_count_values", "winldap/ldap_count_valuesW"]
old-location: ldap\ldap_count_values.htm
tech.root: ldap
ms.assetid: 3b00eeea-a966-4cf1-b945-2f052cae727a
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_count_values, ldap.ldap__count__values, ldap.ldap_count_values, ldap_count_values, ldap_count_values function [LDAP], ldap_count_valuesA, ldap_count_valuesW, winldap/ldap_count_values, winldap/ldap_count_valuesA, winldap/ldap_count_valuesW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_count_valuesW
 - winldap/ldap_count_valuesW
dev_langs:
 - c++
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
---

# ldap_count_valuesW function


## -description

The <b>ldap_count_values</b> function counts the number of values in a list.

## -parameters

### -param vals [in]

An array of null-terminated strings (values) returned by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>.

## -returns

This function returns the number of values in the array. There is no error return.

If a <b>NULL</b> pointer is passed as the argument, 0 is returned. If an invalid argument is passed, the value returned is undefined.

## -remarks

The <b>ldap_count_values</b> function returns the number of values in an array of strings. To count binary values in an array of 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values_len">ldap_count_values_len</a>.





> [!NOTE]
> The winldap.h header defines ldap_count_values as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/previous-versions/windows/desktop/ldap/searching-a-directory">Searching a Directory</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values_len">ldap_count_values_len</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>
