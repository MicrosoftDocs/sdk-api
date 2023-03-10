---
UID: NF:mfapi.DEFINE_MEDIATYPE_GUID
title: DEFINE_MEDIATYPE_GUID macro (mfapi.h)
description: Defines a media subtype GUID from a FOURCC code, D3DFORMAT value, or audio format type.
helpviewer_keywords: ["DEFINE_MEDIATYPE_GUID","DEFINE_MEDIATYPE_GUID macro [Media Foundation]","be094ccc-a475-480a-a345-bdad70b11f45","mf.define_mediatype_guid_macro","mfapi/DEFINE_MEDIATYPE_GUID"]
old-location: mf\define_mediatype_guid_macro.htm
tech.root: mf
ms.assetid: be094ccc-a475-480a-a345-bdad70b11f45
ms.date: 12/05/2018
ms.keywords: DEFINE_MEDIATYPE_GUID, DEFINE_MEDIATYPE_GUID macro [Media Foundation], be094ccc-a475-480a-a345-bdad70b11f45, mf.define_mediatype_guid_macro, mfapi/DEFINE_MEDIATYPE_GUID
req.header: mfapi.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DEFINE_MEDIATYPE_GUID
 - mfapi/DEFINE_MEDIATYPE_GUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - DEFINE_MEDIATYPE_GUID
---

# DEFINE_MEDIATYPE_GUID macro


## -description

Defines a media subtype GUID from a FOURCC code, <b>D3DFORMAT</b> value, or audio format type.

## -parameters

### -param name

The name of the GUID constant to be defined.

### -param format

A FOURCC code, D3DFORMAT value, or audio format type.

## -remarks

Media formats are often identified by a FOURCC code (such as 'AYUV'), <b>D3DFORMAT</b> value (such as D3DFMT_X8R8G8B8), or audio format type (such as WAVE_FORMAT_PCM). The <b>DEFINE_MEDIATYPE_GUID</b> macro defines a new GUID constant from one of these values. The resulting GUID can be used as a media subtype.

This macro invokes the <b>DEFINE_GUID</b> macro. The resulting GUID constant is declared <code>extern</code>, so the declaration must have global scope.


#### Examples


```cpp
#include <initguid.h>

// Declares a GUID named MFVideoFormat_ABCD_Format.
DEFINE_MEDIATYPE_GUID( MFVideoFormat_ABCD_Format, FCC('ABCD') );

```

## -see-also

<a href="/windows/desktop/medfound/mf-mt-subtype-attribute">MF_MT_SUBTYPE</a>



<a href="/windows/desktop/medfound/media-foundation-macros">Media Foundation Macros</a>



<a href="/windows/desktop/medfound/media-type-guids">Media Type GUIDs</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>