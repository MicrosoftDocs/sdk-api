---
UID: NS:winldap.ldapmodW
title: LDAPModW (winldap.h)
description: Holds data required to perform a modification operation. (Unicode)
helpviewer_keywords: ["*PLDAPModW","LDAPMod","LDAPMod structure [LDAP]","LDAPModW","LDAP_MOD_ADD (0x00)","LDAP_MOD_DELETE (0x01)","LDAP_MOD_REPLACE (0x02)","PLDAPMod","PLDAPMod structure pointer [LDAP]","_ldap_ldapmod","ldap.ldapmod","ldapmodA","ldapmodW","winldap/LDAPMod","winldap/PLDAPMod","winldap/ldapmodA","winldap/ldapmodW"]
old-location: ldap\ldapmod.htm
tech.root: ldap
ms.assetid: 07761668-e0d9-4ab0-b8ce-ce8626389e03
ms.date: 12/05/2018
ms.keywords: '*PLDAPModW, LDAPMod, LDAPMod structure [LDAP], LDAPModW, LDAP_MOD_ADD (0x00), LDAP_MOD_DELETE (0x01), LDAP_MOD_REPLACE (0x02), PLDAPMod, PLDAPMod structure pointer [LDAP], _ldap_ldapmod, ldap.ldapmod, ldapmodA, ldapmodW, winldap/LDAPMod, winldap/PLDAPMod, winldap/ldapmodA, winldap/ldapmodW'
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldapmodW (Unicode) and ldapmodA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAPModW, *PLDAPModW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldapmodW
 - winldap/ldapmodW
 - PLDAPModW
 - winldap/PLDAPModW
 - LDAPModW
 - winldap/LDAPModW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winldap.h
api_name:
 - LDAPMod
 - ldapmodA
 - ldapmodW
---

# LDAPModW structure


## -description

The <b>LDAPMod</b> structure holds data required to perform a modification operation.

## -struct-fields

### -field mod_op

Specifies one of the following values to indicate the modification operation to perform.

You can use the bitwise <b>OR</b> operator to combine the operation value with <b>LDAP_MOD_BVALUES</b> to indicate that the <b>mod_vals</b> union uses the <b>modv_bvals</b> member. If <b>LDAP_MOD_BVALUES</b> is not set, the union uses the <b>modv_strvals</b> member.



#### LDAP_MOD_ADD (0x00)

Adds a value to the entry. The supplied values are appended to the existing values in the attribute.



#### LDAP_MOD_DELETE (0x01)

Deletes a value in the entry. The supplied values are deleted from the current attribute values.



#### LDAP_MOD_REPLACE (0x02)

Replaces a value in the entry. The supplied values replace the existing attribute values.

### -field mod_type

Pointer to a null-terminated string that specifies the name of  the attribute to modify.

### -field mod_vals

Pointer to an array of values, if any, to add, delete, or replace. If <b>mop_op</b> does not include the LDAP_MOD_BVALUES flag, the <b>modv_strvals</b> member is a pointer to an array of null-terminated strings. If <b>mop_op</b> includes LDAP_MOD_BVALUES, the <b>modv_bvals</b> member is a pointer to an array of 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> pointers, which is useful for specifying binary values.

### -field mod_vals.modv_strvals

Pointer to a null-terminated array of null-terminated strings. The last element of the array must be a <b>NULL</b> pointer.

### -field mod_vals.modv_bvals

Pointer to a <b>NULL</b>-terminated array of <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> pointers. The last element of the array must be a <b>NULL</b> pointer.


##### - mod_op.LDAP_MOD_ADD (0x00)

Adds a value to the entry. The supplied values are appended to the existing values in the attribute.


##### - mod_op.LDAP_MOD_DELETE (0x01)

Deletes a value in the entry. The supplied values are deleted from the current attribute values.


##### - mod_op.LDAP_MOD_REPLACE (0x02)

Replaces a value in the entry. The supplied values replace the existing attribute values.

## -remarks

Assign values to the fields of the <b>LDAPMod</b> structure before you call a modification function (
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add*</a>, or 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify">ldap_modify*</a>).


<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s">ldap_modify*</a> with the <b>LDAP_MOD_REPLACE</b> operation does not delete an attribute when passed a null pointer. However, <b>LDAP_MOD_DELETE</b> deletes the entire attribute when <b>mod_vals</b> is set to <b>NULL</b>.

When passing a <b>LDAPMod</b> structure into the <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add*</a> functions, only the <b>LDAP_MOD_BVALUES</b> flag is significant. Creating a new object implies adding values to it.





> [!NOTE]
> The winldap.h header defines LDAPMod as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/previous-versions/windows/desktop/ldap/modifying-a-directory-entry">Modifying a Directory Entry</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_add">ldap_add</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify">ldap_modify</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_s">ldap_modify_s</a>
