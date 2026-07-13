---
UID: NS:winldap.ldapcontrolW
title: LDAPControlW (winldap.h)
description: Represents both client-side and server controls. (Unicode)
helpviewer_keywords: ["*PLDAPControlW","LDAPControl","LDAPControl structure [LDAP]","LDAPControlA","LDAPControlW","PLDAPControl","PLDAPControl structure pointer [LDAP]","_ldap_ldapcontrol","ldap.ldapcontrol","winldap/LDAPControl","winldap/LDAPControlA","winldap/LDAPControlW","winldap/PLDAPControl"]
old-location: ldap\ldapcontrol.htm
tech.root: ldap
ms.assetid: c0b4d712-021d-46f3-8bda-aaf660ec1acc
ms.date: 12/05/2018
ms.keywords: '*PLDAPControlW, LDAPControl, LDAPControl structure [LDAP], LDAPControlA, LDAPControlW, PLDAPControl, PLDAPControl structure pointer [LDAP], _ldap_ldapcontrol, ldap.ldapcontrol, winldap/LDAPControl, winldap/LDAPControlA, winldap/LDAPControlW, winldap/PLDAPControl'
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LDAPControlW (Unicode) and LDAPControlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LDAPControlW, *PLDAPControlW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldapcontrolW
 - winldap/ldapcontrolW
 - PLDAPControlW
 - winldap/PLDAPControlW
 - LDAPControlW
 - winldap/LDAPControlW
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
 - LDAPControl
 - LDAPControlA
 - LDAPControlW
---

# LDAPControlW structure


## -description

The <b>LDAPControl</b> structure represents both client-side and server controls.

## -struct-fields

### -field ldctl_oid

Pointer to a wide, null-terminated string that indicates  control type, such as "1.2.840.113556.1.4.805".

### -field ldctl_value

The data associated with the control, if any. If no data is associated with the control, set this member to <b>NULL</b>.

### -field ldctl_iscritical

Indicates whether the control is critical, called the Criticality field.

## -remarks

Effective with LDAP 3, you can extend LDAP operations through the use of controls. Server controls can be sent to the server or returned to the client with any LDAP message. Client controls extend the behavior of the LDAP API on the client-side only and are never sent to the server. A supported control is stored as an object identifier (OID) in the Directory Service root.

The <b>ldctl_iscritical</b> member enables an extended operation to succeed when the server or client does not support the control. If the value of this field is zero, the server and/or client ignores the control if it is not supported and carries out the operation. If the value is nonzero the operation is carried out only if the control is recognized by the server and/or client.

For more information, and a list of the supported LDAP extended controls and their descriptions, see 

<a href="/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>.



> [!NOTE]
> The winldap.h header defines LDAPControl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/data-structures">Data Structures</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>



<a href="/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>

