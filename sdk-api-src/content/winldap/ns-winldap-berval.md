---
UID: NS:winldap.berval
title: berval
author: windows-sdk-content
description: The berval structure represents arbitrary binary data that is encoded according to Basic Encoding Rules (BER). Use a berval to represent any attribute that cannot be represented by a null-terminated string.
old-location: ldap\berval.htm
tech.root: ldap
ms.assetid: 1f279905-ab02-4a8b-9b77-e8ea2b56e882
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PBERVAL, *PLDAP_BERVAL, BERVAL, BERVAL structure [LDAP], BerValue, BerValue structure [LDAP], LDAP_BERVAL, LDAP_BERVAL structure [LDAP], PBERVAL, PBERVAL structure pointer [LDAP], PLDAP_BERVAL, PLDAP_BERVAL structure pointer [LDAP], _ldap_berval, berval, berval structure [LDAP], ldap.berval, winldap/BERVAL, winldap/BerValue, winldap/PBERVAL, winldap/PLDAP_BERVAL, winldap/berval"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - LDAP_BERVAL
product: Windows
targetos: Windows
req.typenames: LDAP_BERVAL, *PLDAP_BERVAL, BERVAL, *PBERVAL, BerValue
req.redist: 
---

# berval structure


## -description


The <b>berval</b> structure represents arbitrary binary data that is encoded according to Basic Encoding Rules (BER). Use a <b>berval</b> to represent any attribute that cannot be represented by a null-terminated string.


## -struct-fields




### -field bv_len

Length, in bytes,  of binary data.


### -field bv_val

Pointer to the binary data.


## -remarks



Use a <b>berval</b> structure for attributes that contain raw binary data, such as certificates, graphics, or sound files.




## -see-also




<a href="https://msdn.microsoft.com/1af7ea80-a65b-42bf-a1b2-ca54c173c9fb">Data Structures</a>
 

 

