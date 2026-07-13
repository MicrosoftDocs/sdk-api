---
UID: NS:dsadmin.DSA_NEWOBJ_DISPINFO
title: DSA_NEWOBJ_DISPINFO (dsadmin.h)
description: Used with the IDsAdminNewObjExt::Initialize method to supply additional data about an Active Directory Domain Services object creation wizard.
helpviewer_keywords: ["*LPDSA_NEWOBJ_DISPINFO","DSA_NEWOBJ_DISPINFO","DSA_NEWOBJ_DISPINFO structure [Active Directory]","LPDSA_NEWOBJ_DISPINFO","LPDSA_NEWOBJ_DISPINFO structure pointer [Active Directory]","ad.dsa_newobj_dispinfo","dsadmin/DSA_NEWOBJ_DISPINFO","dsadmin/LPDSA_NEWOBJ_DISPINFO"]
old-location: ad\dsa_newobj_dispinfo.htm
tech.root: ad
ms.assetid: 966e2093-6ebd-42a0-923d-17f0494a9d0c
ms.date: 12/05/2018
ms.keywords: '*LPDSA_NEWOBJ_DISPINFO, DSA_NEWOBJ_DISPINFO, DSA_NEWOBJ_DISPINFO structure [Active Directory], LPDSA_NEWOBJ_DISPINFO, LPDSA_NEWOBJ_DISPINFO structure pointer [Active Directory], ad.dsa_newobj_dispinfo, dsadmin/DSA_NEWOBJ_DISPINFO, dsadmin/LPDSA_NEWOBJ_DISPINFO'
req.header: dsadmin.h
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
targetos: Windows
req.typenames: DSA_NEWOBJ_DISPINFO, *LPDSA_NEWOBJ_DISPINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDSA_NEWOBJ_DISPINFO
 - dsadmin/LPDSA_NEWOBJ_DISPINFO
 - DSA_NEWOBJ_DISPINFO
 - dsadmin/DSA_NEWOBJ_DISPINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DSAdmin.h
api_name:
 - DSA_NEWOBJ_DISPINFO
---

# DSA_NEWOBJ_DISPINFO structure


## -description

The <b>DSA_NEWOBJ_DISPINFO</b> structure is used with the <a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a> method to supply additional data about an Active Directory Domain Services  object creation wizard.

## -struct-fields

### -field dwSize

Contains the size, in bytes, of the structure. This member is used for versioning purposes.

### -field hObjClassIcon

Contains the handle  of the class icon for the object created.

### -field lpszWizTitle

Pointer to a null-terminated Unicode string that contains the title of the wizard.

### -field lpszContDisplayName

Pointer to a null-terminated Unicode string that contains the display name, or canonical name,  of the container the object is created in.

## -see-also

<a href="/windows/desktop/api/dsadmin/nf-dsadmin-idsadminnewobjext-initialize">IDsAdminNewObjExt::Initialize</a>

