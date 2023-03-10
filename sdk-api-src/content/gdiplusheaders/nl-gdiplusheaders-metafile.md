---
UID: NL:gdiplusheaders.Metafile
title: Metafile (gdiplusheaders.h)
description: The Metafile class defines a graphic metafile. A metafile contains records that describe a sequence of graphics API calls. Metafiles can be recorded (constructed) and played back (displayed).
helpviewer_keywords: ["Metafile","Metafile class [GDI+]","Metafile class [GDI+]","described","_gdiplus_CLASS_Metafile_Class","gdiplus._gdiplus_CLASS_Metafile_Class","gdiplusheaders/Metafile"]
old-location: gdiplus\_gdiplus_CLASS_Metafile_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\metafile.htm
ms.date: 12/05/2018
ms.keywords: Metafile, Metafile class [GDI+], Metafile class [GDI+],described, _gdiplus_CLASS_Metafile_Class, gdiplus._gdiplus_CLASS_Metafile_Class, gdiplusheaders/Metafile
req.header: gdiplusheaders.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Metafile
 - gdiplusheaders/Metafile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Metafile
---

# Metafile class


## -description

The <b>Metafile</b> class defines a graphic metafile. A metafile contains records that describe a sequence of graphics API calls. Metafiles can be recorded (constructed) and played back (displayed).

## -remarks

Some <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-metafile(constmetafile_)">Metafile</a> constructors (those that receive a device context handle) create <b>Metafile</b> objects that are used to record metafiles. Other Metafile constructors (those that do not receive a device context handle) create <b>Metafile</b> objects that are used to display (play back) metafiles.