---
UID: NS:winnt._GENERIC_MAPPING
title: GENERIC_MAPPING (winnt.h)
description: Defines the mapping of generic access rights to specific and standard access rights for an object.
helpviewer_keywords: ["*PGENERIC_MAPPING","GENERIC_MAPPING","GENERIC_MAPPING structure [Security]","PGENERIC_MAPPING","PGENERIC_MAPPING structure pointer [Security]","_GENERIC_MAPPING","_win32_generic_mapping_str","security.generic_mapping","winnt/GENERIC_MAPPING","winnt/PGENERIC_MAPPING"]
old-location: security\generic_mapping.htm
tech.root: security
ms.assetid: e3c49b47-9bc7-4000-a131-449345ebb9cd
ms.date: 12/05/2018
ms.keywords: '*PGENERIC_MAPPING, GENERIC_MAPPING, GENERIC_MAPPING structure [Security], PGENERIC_MAPPING, PGENERIC_MAPPING structure pointer [Security], _GENERIC_MAPPING, _win32_generic_mapping_str, security.generic_mapping, winnt/GENERIC_MAPPING, winnt/PGENERIC_MAPPING'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: GENERIC_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GENERIC_MAPPING
 - winnt/_GENERIC_MAPPING
 - GENERIC_MAPPING
 - winnt/GENERIC_MAPPING
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
 - GENERIC_MAPPING
---

# GENERIC_MAPPING structure


## -description

The <b>GENERIC_MAPPING</b> structure defines the mapping of generic access rights to specific and standard access rights for an object. When a client application requests generic access to an object, that request is mapped to the access rights defined in this structure.

## -struct-fields

### -field GenericRead

Specifies an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> defining read access to an object.

### -field GenericWrite

Specifies an access mask defining write access to an object.

### -field GenericExecute

Specifies an access mask defining execute access to an object.

### -field GenericAll

Specifies an access mask defining all possible types of access to an object.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckandauditalarma">AccessCheckAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>