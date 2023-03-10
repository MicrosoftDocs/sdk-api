---
UID: NS:strmif.tagVMRPRESENTATIONINFO
title: VMRPRESENTATIONINFO (strmif.h)
description: The VMRPRESENTATIONINFO structure is used in the IVMRImagePresenter::PresentImage method (VMR-7 only).
helpviewer_keywords: ["VMRPRESENTATIONINFO","VMRPRESENTATIONINFO structure [DirectShow]","VMRPRESENTATIONINFOStructure","dshow.vmrpresentationinfo","strmif/VMRPRESENTATIONINFO"]
old-location: dshow\vmrpresentationinfo.htm
tech.root: dshow
ms.assetid: cddbe3de-c5e2-4161-801f-f3497714922c
ms.date: 12/05/2018
ms.keywords: VMRPRESENTATIONINFO, VMRPRESENTATIONINFO structure [DirectShow], VMRPRESENTATIONINFOStructure, dshow.vmrpresentationinfo, strmif/VMRPRESENTATIONINFO
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: VMRPRESENTATIONINFO
req.redist: 
req.product: Windows XP
ms.custom: 19H1
f1_keywords:
 - tagVMRPRESENTATIONINFO
 - strmif/tagVMRPRESENTATIONINFO
 - VMRPRESENTATIONINFO
 - strmif/VMRPRESENTATIONINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRPRESENTATIONINFO
---

# VMRPRESENTATIONINFO structure


## -description

The <code>VMRPRESENTATIONINFO</code> structure is used in the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenter-presentimage">IVMRImagePresenter::PresentImage</a> method (VMR-7 only).

## -struct-fields

### -field dwFlags

A bitwise combination of flags from the <a href="/windows/desktop/api/strmif/ne-strmif-vmrpresentationflags">VMRPresentationFlags</a> enumeration, which describe the status of the video sample with respect to its presentation time.

### -field lpSurf

Pointer to the DirectDraw surface that contains the video frame to be presented.

### -field rtStart

The start time for the current frame, in 100-nanosecond units.

### -field rtEnd

The end time for the current frame, in 100-nanosecond units.

### -field szAspectRatio

The aspect ratio of the rectangle.

### -field rcSrc

The source rectangle.

### -field rcDst

The destination rectangle.

### -field dwTypeSpecificFlags

Bitwise combination of flags, as defined for the [AM_SAMPLE2_PROPERTIES](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.

### -field dwInterlaceFlags

Bitwise combination of flags, as defined for the <b>dwInterlaceFlags</b> member of the <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a>