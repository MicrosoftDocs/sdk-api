---
UID: NS:msime._IMESHF
title: IMESHF (msime.h)
description: The header of an opened user dictionary file. Used to get the user dictionary's properties, such as version, title, description, and copyright.
helpviewer_keywords: ["IMESHF","IMESHF structure [Internationalization for Windows Applications]","PIMESHF","PIMESHF structure pointer [Internationalization for Windows Applications]","intl.imeshf","msime/IMESHF","msime/PIMESHF"]
old-location: intl\imeshf.htm
tech.root: Intl
ms.assetid: CFFEFEDC-F614-4DD4-B1A1-4D236339E817
ms.date: 12/05/2018
ms.keywords: IMESHF, IMESHF structure [Internationalization for Windows Applications], PIMESHF, PIMESHF structure pointer [Internationalization for Windows Applications], intl.imeshf, msime/IMESHF, msime/PIMESHF
req.header: msime.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMESHF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMESHF
 - msime/_IMESHF
 - IMESHF
 - msime/IMESHF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msime.h
api_name:
 - IMESHF
---

# IMESHF structure


## -description

The header of an opened user dictionary file. Used to get the user dictionary's properties, such as version, title, description, and copyright.

## -struct-fields

### -field cbShf

The size of this structure. You must set this value before using the structure.

### -field verDic

Dictionary version.

### -field szTitle

Dictionary title.

### -field szDescription

Dictionary description.

### -field szCopyright

Dictionary copyright information.

## -see-also

<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-create">IFEDictionary::Create</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-getheader">IFEDictionary::GetHeader</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-open">IFEDictionary::Open</a>



<a href="/windows/desktop/api/msime/nf-msime-ifedictionary-setheader">IFEDictionary::SetHeader</a>