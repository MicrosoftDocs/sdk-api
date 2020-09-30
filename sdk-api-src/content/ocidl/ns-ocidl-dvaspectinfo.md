---
UID: NS:ocidl.tagAspectInfo
title: DVASPECTINFO (ocidl.h)
description: Contains information that is used by the IViewObject::Draw method to optimize rendering of an inactive object by making more efficient use of the GDI.
helpviewer_keywords: ["DVASPECTINFO","DVASPECTINFO structure [COM]","_ole_DVASPECTINFO","com.dvaspectinfo","ocidl/DVASPECTINFO"]
old-location: com\dvaspectinfo.htm
tech.root: com
ms.assetid: c9375b9d-c822-4322-ba6f-967792257672
ms.date: 12/05/2018
ms.keywords: DVASPECTINFO, DVASPECTINFO structure [COM], _ole_DVASPECTINFO, com.dvaspectinfo, ocidl/DVASPECTINFO
req.header: ocidl.h
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
req.typenames: DVASPECTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAspectInfo
 - ocidl/tagAspectInfo
 - DVASPECTINFO
 - ocidl/DVASPECTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - DVASPECTINFO
---

# DVASPECTINFO structure


## -description

Contains information that is used by the <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> method to optimize rendering of an inactive object by making more efficient use of the GDI.

## -struct-fields

### -field cb

The size of the structure, in bytes.

### -field dwFlags

A value taken from the <a href="/windows/win32/api/ocidl/ne-ocidl-dvaspectinfoflag">DVASPECTINFOFLAG</a> enumeration.

## -see-also

<a href="/windows/win32/api/ocidl/ne-ocidl-dvaspectinfoflag">DVASPECTINFOFLAG</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>