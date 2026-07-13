---
UID: NE:mgm._MGM_ENUM_TYPES
title: MGM_ENUM_TYPES (mgm.h)
description: The MGM_ENUM_TYPES enumeration lists the types of group enumerations that the multicast group manager uses. This structure is used by the MgmGroupEnumerationStart function.
helpviewer_keywords: ["ALL_SOURCES","ANY_SOURCE","MGM_ENUM_TYPES","MGM_ENUM_TYPES enumeration [RAS]","_mpr_mgm_enum_types","mgm/ALL_SOURCES","mgm/ANY_SOURCE","mgm/MGM_ENUM_TYPES","rras.mgm_enum_types"]
old-location: rras\mgm_enum_types.htm
tech.root: RRAS
ms.assetid: 09b60342-25a8-4d0a-8176-3701f0622aa8
ms.date: 12/05/2018
ms.keywords: ALL_SOURCES, ANY_SOURCE, MGM_ENUM_TYPES, MGM_ENUM_TYPES enumeration [RAS], _mpr_mgm_enum_types, mgm/ALL_SOURCES, mgm/ANY_SOURCE, mgm/MGM_ENUM_TYPES, rras.mgm_enum_types
req.header: mgm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MGM_ENUM_TYPES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MGM_ENUM_TYPES
 - mgm/_MGM_ENUM_TYPES
 - MGM_ENUM_TYPES
 - mgm/MGM_ENUM_TYPES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mgm.h
api_name:
 - MGM_ENUM_TYPES
---

# MGM_ENUM_TYPES enumeration


## -description

The 
<b>MGM_ENUM_TYPES</b> enumeration lists the types of group enumerations that the multicast group manager uses. This structure is used by the 
<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a> function.

## -enum-fields

### -field ANY_SOURCE:0

Enumerate group entries that have at least one source.

### -field ALL_SOURCES

Enumerate all source entries for a group.

## -see-also

<a href="/windows/desktop/api/mgm/nf-mgm-mgmgroupenumerationstart">MgmGroupEnumerationStart</a>
