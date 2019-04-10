---
UID: NS:winldap.ldapcontrolW
title: LDAPControlW (winldap.h)
author: windows-sdk-content
description: Represents both client-side and server controls.
old-location: ldap\ldapcontrol.htm
tech.root: ldap
ms.assetid: c0b4d712-021d-46f3-8bda-aaf660ec1acc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PLDAPControlW, LDAPControl, LDAPControl structure [LDAP], LDAPControlA, LDAPControlW, PLDAPControl, PLDAPControl structure pointer [LDAP], _ldap_ldapcontrol, ldap.ldapcontrol, winldap/LDAPControl, winldap/LDAPControlA, winldap/LDAPControlW, winldap/PLDAPControl"
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: LDAPControlW, *PLDAPControlW
req.redist: 
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
<a href="https://msdn.microsoft.com/3e1e29ff-43ec-4cc3-9414-41b7c61f8b42">Extended Controls</a>.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>



<a href="https://msdn.microsoft.com/547a0736-23a4-4bfd-8ae0-866825228b53">LDAPMessage</a>



<a href="https://msdn.microsoft.com/2c1f68e6-51b0-4270-b55a-88ba7292bbbc">Using Controls</a>
 

 

