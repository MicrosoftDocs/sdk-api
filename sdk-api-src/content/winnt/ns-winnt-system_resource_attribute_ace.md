---
UID: NS:winnt._SYSTEM_RESOURCE_ATTRIBUTE_ACE
title: SYSTEM_RESOURCE_ATTRIBUTE_ACE (winnt.h)
description: Defines an access control entry (ACE) for the system access control list (SACL) that specifies the system resource attributes for a securable object.
helpviewer_keywords: ["*PSYSTEM_RESOURCE_ATTRIBUTE_ACE","PSYSTEM_RESOURCE_ATTRIBUTE_ACE","PSYSTEM_RESOURCE_ATTRIBUTE_ACE structure pointer [Security]","SYSTEM_RESOURCE_ATTRIBUTE_ACE","SYSTEM_RESOURCE_ATTRIBUTE_ACE structure [Security]","_SYSTEM_RESOURCE_ATTRIBUTE_ACE","security.system_resource_attribute_ace","winnt/PSYSTEM_RESOURCE_ATTRIBUTE_ACE","winnt/SYSTEM_RESOURCE_ATTRIBUTE_ACE"]
old-location: security\system_resource_attribute_ace.htm
tech.root: security
ms.assetid: A222E1B7-CA9C-4250-A697-B9D278B26C06
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_RESOURCE_ATTRIBUTE_ACE, PSYSTEM_RESOURCE_ATTRIBUTE_ACE, PSYSTEM_RESOURCE_ATTRIBUTE_ACE structure pointer [Security], SYSTEM_RESOURCE_ATTRIBUTE_ACE, SYSTEM_RESOURCE_ATTRIBUTE_ACE structure [Security], _SYSTEM_RESOURCE_ATTRIBUTE_ACE, security.system_resource_attribute_ace, winnt/PSYSTEM_RESOURCE_ATTRIBUTE_ACE, winnt/SYSTEM_RESOURCE_ATTRIBUTE_ACE'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: SYSTEM_RESOURCE_ATTRIBUTE_ACE, *PSYSTEM_RESOURCE_ATTRIBUTE_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_RESOURCE_ATTRIBUTE_ACE
 - winnt/_SYSTEM_RESOURCE_ATTRIBUTE_ACE
 - PSYSTEM_RESOURCE_ATTRIBUTE_ACE
 - winnt/PSYSTEM_RESOURCE_ATTRIBUTE_ACE
 - SYSTEM_RESOURCE_ATTRIBUTE_ACE
 - winnt/SYSTEM_RESOURCE_ATTRIBUTE_ACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SYSTEM_RESOURCE_ATTRIBUTE_ACE
---

# SYSTEM_RESOURCE_ATTRIBUTE_ACE structure


## -description

The <b>SYSTEM_RESOURCE_ATTRIBUTE_ACE</b> structure defines an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that specifies the system resource attributes for a securable object.

## -struct-fields

### -field Header

An <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of the ACE. The structure also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure must be set to <b>SYSTEM_RESOURCE_ATTRIBUTE_ACE</b>, and the <b>AceSize</b> member must be set to the total number of bytes allocated for the <b>SYSTEM_RESOURCE_ATTRIBUTE_ACE</b> structure.

### -field Mask

The access policy associated with the SACL that contains this ACE.

### -field SidStart

Specifies the first <b>DWORD</b> of a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>. The remaining bytes of the <b>SID</b>  are stored in contiguous memory after the <b>SidStart</b> member in a <a href="/windows/desktop/api/winnt/ns-winnt-claim_security_attribute_relative_v1">CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1</a> structure.