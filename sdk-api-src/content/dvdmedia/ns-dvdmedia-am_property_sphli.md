---
UID: NS:dvdmedia._AM_PROPERTY_SPHLI
title: AM_PROPERTY_SPHLI (dvdmedia.h)
description: Describes the currently selected button from the DVD highlight information.
helpviewer_keywords: ["*PAM_PROPERTY_SPHLI","AM_PROPERTY_SPHLI","AM_PROPERTY_SPHLI structure [DirectShow]","PAM_PROPERTY_SPHLI","PAM_PROPERTY_SPHLI structure pointer [DirectShow]","dshow.am_property_sphli","dvdmedia/AM_PROPERTY_SPHLI","dvdmedia/PAM_PROPERTY_SPHLI"]
old-location: dshow\am_property_sphli.htm
tech.root: dshow
ms.assetid: fc073d53-bebb-47fc-b60c-7467b4df88c1
ms.date: 12/05/2018
ms.keywords: '*PAM_PROPERTY_SPHLI, AM_PROPERTY_SPHLI, AM_PROPERTY_SPHLI structure [DirectShow], PAM_PROPERTY_SPHLI, PAM_PROPERTY_SPHLI structure pointer [DirectShow], dshow.am_property_sphli, dvdmedia/AM_PROPERTY_SPHLI, dvdmedia/PAM_PROPERTY_SPHLI'
req.header: dvdmedia.h
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
req.typenames: AM_PROPERTY_SPHLI, *PAM_PROPERTY_SPHLI
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_PROPERTY_SPHLI
 - dvdmedia/_AM_PROPERTY_SPHLI
 - PAM_PROPERTY_SPHLI
 - dvdmedia/PAM_PROPERTY_SPHLI
 - AM_PROPERTY_SPHLI
 - dvdmedia/AM_PROPERTY_SPHLI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_PROPERTY_SPHLI
---

# AM_PROPERTY_SPHLI structure


## -description

Describes the currently selected button from the DVD highlight information.

## -struct-fields

### -field HLISS

Highlight status of current selection.

### -field Reserved

Reserved for internal use. Do not use or set.

### -field StartPTM

Start presentation time divided by 90,000.

### -field EndPTM

End presentation time divided by 90,000.

### -field StartX

Start x-coordinate pixel of the current highlight button.

### -field StartY

Start y-coordinate pixel of the current highlight button.

### -field StopX

Ending x-coordinate pixel of the current highlight button.

### -field StopY

Ending y-coordinate pixel of the current highlight button.

### -field ColCon

Color contrast description of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_colcon">AM_COLCON</a>.

## -remarks

The <b>AM_PROPERTY_DVDSUBPIC_HLI</b> property uses this structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-subpicture-property-set">DVD Subpicture Property Set</a>