---
UID: NS:winnt._SID_AND_ATTRIBUTES_HASH
title: SID_AND_ATTRIBUTES_HASH (winnt.h)
description: Specifies a hash values for the specified array of security identifiers (SIDs).
helpviewer_keywords: ["*PSID_AND_ATTRIBUTES_HASH","PSID_AND_ATTRIBUTES_HASH","PSID_AND_ATTRIBUTES_HASH structure pointer [Security]","SID_AND_ATTRIBUTES_HASH","SID_AND_ATTRIBUTES_HASH structure [Security]","_SID_AND_ATTRIBUTES_HASH","security.sid_and_attributes_hash","winnt/PSID_AND_ATTRIBUTES_HASH","winnt/SID_AND_ATTRIBUTES_HASH"]
old-location: security\sid_and_attributes_hash.htm
tech.root: security
ms.assetid: ef6e32f5-b47e-463e-a447-bed149b8d616
ms.date: 12/05/2018
ms.keywords: '*PSID_AND_ATTRIBUTES_HASH, PSID_AND_ATTRIBUTES_HASH, PSID_AND_ATTRIBUTES_HASH structure pointer [Security], SID_AND_ATTRIBUTES_HASH, SID_AND_ATTRIBUTES_HASH structure [Security], _SID_AND_ATTRIBUTES_HASH, security.sid_and_attributes_hash, winnt/PSID_AND_ATTRIBUTES_HASH, winnt/SID_AND_ATTRIBUTES_HASH'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SID_AND_ATTRIBUTES_HASH, *PSID_AND_ATTRIBUTES_HASH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SID_AND_ATTRIBUTES_HASH
 - winnt/_SID_AND_ATTRIBUTES_HASH
 - PSID_AND_ATTRIBUTES_HASH
 - winnt/PSID_AND_ATTRIBUTES_HASH
 - SID_AND_ATTRIBUTES_HASH
 - winnt/SID_AND_ATTRIBUTES_HASH
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
 - SID_AND_ATTRIBUTES_HASH
---

# SID_AND_ATTRIBUTES_HASH structure


## -description

The <b>SID_AND_ATTRIBUTES_HASH</b> structure specifies a hash values for the specified array of <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).

## -struct-fields

### -field SidCount

The number of SIDs pointed to by the <i>SidAttr</i> parameter.

### -field SidAttr

A pointer to an array of <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structures that represent SIDs and their attributes.

### -field Hash

An array of pointers to hash values. These values correspond to the <a href="/windows/desktop/api/winnt/ns-winnt-sid_and_attributes">SID_AND_ATTRIBUTES</a> structures pointed to by the <i>SidAttr</i> parameter.

The <b>SID_HASH_ENTRY</b> data type is defined in Winnt.h as a <b>ULONG_PTR</b>.

The <b>SID_HASH_SIZE</b> array dimension is defined in Winnt.h as 32.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-token_access_information">TOKEN_ACCESS_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ne-winnt-token_information_class">TOKEN_INFORMATION_CLASS</a>