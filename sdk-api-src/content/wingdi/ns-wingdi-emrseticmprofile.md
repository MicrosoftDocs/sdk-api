---
UID: NS:wingdi.tagEMRSETICMPROFILE
title: EMRSETICMPROFILE (wingdi.h)
description: The EMRSETICMPROFILE structure contains members for the SetICMProfile enhanced metafile record.
helpviewer_keywords: ["*PEMRSETICMPROFILE","*PEMRSETICMPROFILEA","*PEMRSETICMPROFILEW","EMRSETICMPROFILE","EMRSETICMPROFILE structure [Windows GDI]","EMRSETICMPROFILEA","EMRSETICMPROFILEA structure [Windows GDI]","EMRSETICMPROFILEW","EMRSETICMPROFILEW structure [Windows GDI]","PEMRSETICMPROFILE","PEMRSETICMPROFILE structure pointer [Windows GDI]","PEMRSETICMPROFILEA","PEMRSETICMPROFILEA structure pointer [Windows GDI]","PEMRSETICMPROFILEW","PEMRSETICMPROFILEW structure pointer [Windows GDI]","_win32_EMRSETICMPROFILE_str","gdi.emrseticmprofile","wingdi/EMRSETICMPROFILE","wingdi/EMRSETICMPROFILEA","wingdi/EMRSETICMPROFILEW","wingdi/PEMRSETICMPROFILE","wingdi/PEMRSETICMPROFILEA","wingdi/PEMRSETICMPROFILEW"]
old-location: gdi\emrseticmprofile.htm
tech.root: gdi
ms.assetid: 2f43db1e-95eb-4812-9422-ddc9df634c15
ms.date: 12/05/2018
ms.keywords: '*PEMRSETICMPROFILE, *PEMRSETICMPROFILEA, *PEMRSETICMPROFILEW, EMRSETICMPROFILE, EMRSETICMPROFILE structure [Windows GDI], EMRSETICMPROFILEA, EMRSETICMPROFILEA structure [Windows GDI], EMRSETICMPROFILEW, EMRSETICMPROFILEW structure [Windows GDI], PEMRSETICMPROFILE, PEMRSETICMPROFILE structure pointer [Windows GDI], PEMRSETICMPROFILEA, PEMRSETICMPROFILEA structure pointer [Windows GDI], PEMRSETICMPROFILEW, PEMRSETICMPROFILEW structure pointer [Windows GDI], _win32_EMRSETICMPROFILE_str, gdi.emrseticmprofile, wingdi/EMRSETICMPROFILE, wingdi/EMRSETICMPROFILEA, wingdi/EMRSETICMPROFILEW, wingdi/PEMRSETICMPROFILE, wingdi/PEMRSETICMPROFILEA, wingdi/PEMRSETICMPROFILEW'
req.header: wingdi.h
req.include-header: Windows.h
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
req.typenames: EMRSETICMPROFILE, *PEMRSETICMPROFILE, EMRSETICMPROFILEA, *PEMRSETICMPROFILEA, EMRSETICMPROFILEW, *PEMRSETICMPROFILEW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEMRSETICMPROFILE
 - wingdi/tagEMRSETICMPROFILE
 - PEMRSETICMPROFILE
 - wingdi/PEMRSETICMPROFILE
 - EMRSETICMPROFILE
 - wingdi/EMRSETICMPROFILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EMRSETICMPROFILE
---

# EMRSETICMPROFILE structure


## -description

The <b>EMRSETICMPROFILE</b> structure contains members for the <a href="/windows/desktop/api/wingdi/nf-wingdi-seticmprofilea">SetICMProfile</a> enhanced metafile record.

## -struct-fields

### -field emr

The base structure for all record types.

### -field dwFlags

The profile flags. This member can be SETICMPROFILE_EMBEDED (0x00000001).

### -field cbName

The size of the desired profile name.

### -field cbData

The size of profile data, if attached.

### -field Data

An array that contains the profile data. The length of this array is <b>cbName</b> plus <b>cbData</b>.

## -remarks

This structure is to be used during metafile playback.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-emr">EMR</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-seticmprofilea">SetICMProfile</a>