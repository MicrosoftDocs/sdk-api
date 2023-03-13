---
UID: NE:objbase.tagCOMSD
title: COMSD (objbase.h)
description: Determines the type of COM security descriptor to get when calling CoGetSystemSecurityPermissions.
helpviewer_keywords: ["COMSD","COMSD enumeration [COM]","SD_ACCESSPERMISSIONS","SD_ACCESSRESTRICTIONS","SD_LAUNCHPERMISSIONS","SD_LAUNCHRESTRICTIONS","com.comsd","objbase/COMSD","objbase/SD_ACCESSPERMISSIONS","objbase/SD_ACCESSRESTRICTIONS","objbase/SD_LAUNCHPERMISSIONS","objbase/SD_LAUNCHRESTRICTIONS"]
old-location: com\comsd.htm
tech.root: com
ms.assetid: FF783F27-D5EF-4927-9B7D-489271FBA9B3
ms.date: 12/05/2018
ms.keywords: COMSD, COMSD enumeration [COM], SD_ACCESSPERMISSIONS, SD_ACCESSRESTRICTIONS, SD_LAUNCHPERMISSIONS, SD_LAUNCHRESTRICTIONS, com.comsd, objbase/COMSD, objbase/SD_ACCESSPERMISSIONS, objbase/SD_ACCESSRESTRICTIONS, objbase/SD_LAUNCHPERMISSIONS, objbase/SD_LAUNCHRESTRICTIONS
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: COMSD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCOMSD
 - objbase/tagCOMSD
 - COMSD
 - objbase/COMSD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objbase.h
api_name:
 - COMSD
---

# COMSD enumeration


## -description

Determines the type of COM security descriptor to get when calling <a href="/windows/desktop/api/objbase/nf-objbase-cogetsystemsecuritypermissions">CoGetSystemSecurityPermissions</a>.

## -enum-fields

### -field SD_LAUNCHPERMISSIONS:0

Machine-wide launch permissions.

### -field SD_ACCESSPERMISSIONS:1

Machine-wide access permissions.

### -field SD_LAUNCHRESTRICTIONS:2

Machine-wide launch limits.

### -field SD_ACCESSRESTRICTIONS:3       

Machine-wide access limits.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-cogetsystemsecuritypermissions">CoGetSystemSecurityPermissions</a>
