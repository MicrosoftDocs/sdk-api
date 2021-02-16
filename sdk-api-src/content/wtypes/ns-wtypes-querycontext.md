---
UID: NS:wtypes.tagQUERYCONTEXT
title: QUERYCONTEXT (wtypes.h)
description: Contains a list of attributes used to look up a class implementation.
helpviewer_keywords: ["QUERYCONTEXT","QUERYCONTEXT structure [COM]","_com_QUERYCONTEXT","com.querycontext","wtypes/tagQUERYCONTEXT"]
old-location: com\querycontext.htm
tech.root: com
ms.assetid: 5d6a17e1-dcdd-4691-aec2-f63dbcb26027
ms.date: 12/05/2018
ms.keywords: QUERYCONTEXT, QUERYCONTEXT structure [COM], _com_QUERYCONTEXT, com.querycontext, wtypes/tagQUERYCONTEXT
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
req.typenames: QUERYCONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQUERYCONTEXT
 - wtypes/tagQUERYCONTEXT
 - QUERYCONTEXT
 - wtypes/QUERYCONTEXT
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
 - QUERYCONTEXT
---

# QUERYCONTEXT structure


## -description

Contains a list of attributes used to look up a class implementation.

## -struct-fields

### -field dwContext

The execution context.

### -field Platform

The operating system platform and processor architecture. For more information, see <a href="/windows/desktop/api/wtypes/ns-wtypes-csplatform">CSPLATFORM</a>.

### -field Locale

The locale identifier. For more information, see <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Language Identifier Constants and Strings</a>.

### -field dwVersionHi

The high version number.

### -field dwVersionLo

The low version number.

## -see-also

<a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coinstall">CoInstall</a>