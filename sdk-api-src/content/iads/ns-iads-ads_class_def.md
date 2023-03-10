---
UID: NS:iads._ads_class_def
title: ADS_CLASS_DEF (iads.h)
description: The ADS_CLASS_DEF structure is used only as a part of IDirectorySchemaMgmt, which is an obsolete interface. The information that follows is provided for legacy purposes only. The ADS_CLASS_DEF structure holds the definitions of an object class.
helpviewer_keywords: ["*PADS_CLASS_DEF","ADS_CLASS_DEF","ADS_CLASS_DEF structure [ADSI]","PADS_CLASS_DEF","PADS_CLASS_DEF structure pointer [ADSI]","_ds_ads_class_def","adsi.ads__class__def","adsi.ads_class_def","iads/ADS_CLASS_DEF","iads/PADS_CLASS_DEF"]
old-location: adsi\ads_class_def.htm
tech.root: adsi
ms.assetid: 8151977a-bd98-439f-91ae-6052970ea47c
ms.date: 12/05/2018
ms.keywords: '*PADS_CLASS_DEF, ADS_CLASS_DEF, ADS_CLASS_DEF structure [ADSI], PADS_CLASS_DEF, PADS_CLASS_DEF structure pointer [ADSI], _ds_ads_class_def, adsi.ads__class__def, adsi.ads_class_def, iads/ADS_CLASS_DEF, iads/PADS_CLASS_DEF'
req.header: iads.h
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
req.typenames: ADS_CLASS_DEF, *PADS_CLASS_DEF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ads_class_def
 - iads/_ads_class_def
 - PADS_CLASS_DEF
 - iads/PADS_CLASS_DEF
 - ADS_CLASS_DEF
 - iads/ADS_CLASS_DEF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_CLASS_DEF
---

# ADS_CLASS_DEF structure


## -description

The <b>ADS_CLASS_DEF</b> structure is used only as a part of <b>IDirectorySchemaMgmt</b>, which is an obsolete interface.  The information that follows is provided for legacy purposes only.
   

The <b>ADS_CLASS_DEF</b> structure holds the definitions of an object class.

## -struct-fields

### -field pszClassName

The null-terminated Unicode string that specifies the class name.

### -field dwMandatoryAttrs

The number of mandatory class attributes.

### -field ppszMandatoryAttrs

Pointer to an array of  null-terminated Unicode strings that contain the names of the mandatory attributes.

### -field optionalAttrs

Number of optional attributes of the class.

### -field ppszOptionalAttrs

Pointer to an array of null-terminated Unicode strings that contain the names of the optional attributes.

### -field dwNamingAttrs

Number of naming attributes.

### -field ppszNamingAttrs

Pointer to an array of null-terminated Unicode strings that contain the names of the naming attributes.

### -field dwSuperClasses

Number of super classes of an object of this class.

### -field ppszSuperClasses

Pointer to an array of null-terminated Unicode strings that contain the names of the super classes.

### -field fIsContainer

Flags that indicate the object of the class is a container when it is <b>TRUE</b> and not a container when <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>