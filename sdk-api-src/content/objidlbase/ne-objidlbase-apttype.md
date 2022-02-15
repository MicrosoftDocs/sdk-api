---
UID: NE:objidlbase._APTTYPE
title: APTTYPE (objidlbase.h)
description: Specifies different types of apartments.
helpviewer_keywords: ["APTTYPE","APTTYPE enumeration [COM]","APTTYPE_CURRENT","APTTYPE_MAINSTA","APTTYPE_MTA","APTTYPE_NA","APTTYPE_STA","_com_APTTYPE","com.apttype","objidlbase/APTTYPE","objidlbase/APTTYPE_CURRENT","objidlbase/APTTYPE_MAINSTA","objidlbase/APTTYPE_MTA","objidlbase/APTTYPE_NA","objidlbase/APTTYPE_STA"]
old-location: com\apttype.htm
tech.root: com
ms.assetid: eae95b1f-3883-4334-aa7e-84e71e05fb24
ms.date: 12/05/2018
ms.keywords: APTTYPE, APTTYPE enumeration [COM], APTTYPE_CURRENT, APTTYPE_MAINSTA, APTTYPE_MTA, APTTYPE_NA, APTTYPE_STA, _com_APTTYPE, com.apttype, objidlbase/APTTYPE, objidlbase/APTTYPE_CURRENT, objidlbase/APTTYPE_MAINSTA, objidlbase/APTTYPE_MTA, objidlbase/APTTYPE_NA, objidlbase/APTTYPE_STA
req.header: objidlbase.h
req.include-header: Objidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: APTTYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _APTTYPE
 - objidlbase/_APTTYPE
 - APTTYPE
 - objidlbase/APTTYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - objidlbase.h
api_name:
 - APTTYPE
---

# APTTYPE enumeration


## -description

Specifies different types of apartments.

## -enum-fields

### -field APTTYPE_CURRENT:-1

The current thread.

### -field APTTYPE_STA:0

A single-threaded apartment.

### -field APTTYPE_MTA:1

A multithreaded apartment.

### -field APTTYPE_NA:2

A neutral apartment.

### -field APTTYPE_MAINSTA:3

The main single-threaded apartment.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetapartmenttype">CoGetApartmentType</a>



<a href="/windows/desktop/api/objidl/nf-objidl-icomthreadinginfo-getcurrentapartmenttype">IComThreadingInfo::GetCurrentApartmentType</a>
