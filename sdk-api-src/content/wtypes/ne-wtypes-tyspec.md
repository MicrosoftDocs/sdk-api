---
UID: NE:wtypes.tagTYSPEC
title: TYSPEC (wtypes.h)
description: Specifies a mapping for a class ID.
helpviewer_keywords: ["TYSPEC","TYSPEC enumeration [COM]","TYSPEC_CLSID","TYSPEC_FILEEXT","TYSPEC_FILENAME","TYSPEC_MIMETYPE","TYSPEC_OBJECTID","TYSPEC_PACKAGENAME","TYSPEC_PROGID","_com_TYSPEC","com.tyspec","wtypes/TYSPEC","wtypes/TYSPEC_CLSID","wtypes/TYSPEC_FILEEXT","wtypes/TYSPEC_FILENAME","wtypes/TYSPEC_MIMETYPE","wtypes/TYSPEC_OBJECTID","wtypes/TYSPEC_PACKAGENAME","wtypes/TYSPEC_PROGID"]
old-location: com\tyspec.htm
tech.root: com
ms.assetid: f2972300-5a95-43e3-b2d1-cd8f30d14d1d
ms.date: 12/05/2018
ms.keywords: TYSPEC, TYSPEC enumeration [COM], TYSPEC_CLSID, TYSPEC_FILEEXT, TYSPEC_FILENAME, TYSPEC_MIMETYPE, TYSPEC_OBJECTID, TYSPEC_PACKAGENAME, TYSPEC_PROGID, _com_TYSPEC, com.tyspec, wtypes/TYSPEC, wtypes/TYSPEC_CLSID, wtypes/TYSPEC_FILEEXT, wtypes/TYSPEC_FILENAME, wtypes/TYSPEC_MIMETYPE, wtypes/TYSPEC_OBJECTID, wtypes/TYSPEC_PACKAGENAME, wtypes/TYSPEC_PROGID
req.header: wtypes.h
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
req.typenames: TYSPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTYSPEC
 - wtypes/tagTYSPEC
 - TYSPEC
 - wtypes/TYSPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WTypes.h
api_name:
 - TYSPEC
---

# TYSPEC enumeration


## -description

Specifies a mapping for a class ID.

## -enum-fields

### -field TYSPEC_CLSID:0

A CLSID.

### -field TYSPEC_FILEEXT

A file name extension.

### -field TYSPEC_MIMETYPE

A MIME type.

### -field TYSPEC_FILENAME

A file name.

### -field TYSPEC_PROGID

A PROGID.

### -field TYSPEC_PACKAGENAME

A package name.

### -field TYSPEC_OBJECTID

An object ID.

## -remarks

The TYSPEC enumeration and uCLSSPEC union provide mappings to a class ID. Note that TYSPEC_CLSID is the only supported value.


``` syntax
    typedef union switch(DWORD tyspec)
        {
        case TYSPEC_CLSID:
            CLSID   clsid;
        case TYSPEC_FILEEXT:
            LPOLESTR pFileExt;
        case TYSPEC_MIMETYPE:
            LPOLESTR pMimeType;
        case TYSPEC_PROGID:
            LPOLESTR pProgId;
        case TYSPEC_FILENAME:
            LPOLESTR pFileName;
        case TYSPEC_PACKAGENAME:
            struct {
            LPOLESTR pPackageName;
            GUID     PolicyId;
            } ByName;
        case TYSPEC_OBJECTID:
            struct {
            GUID     ObjectId;
            GUID     PolicyId;
            } ByObjectId;
    } uCLSSPEC;
```


## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-coinstall">CoInstall</a>
