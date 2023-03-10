---
UID: NS:dvdmedia._DVD_REGION
title: DVD_REGION (dvdmedia.h)
description: Identifies the DVD region as reported by the local system components.
helpviewer_keywords: ["*PDVD_REGION","DVD_REGION","DVD_REGION structure [DirectShow]","DVD_REGIONStructure","PDVD_REGION","PDVD_REGION structure pointer [DirectShow]","dshow.dvd_region","dvdmedia/DVD_REGION","dvdmedia/PDVD_REGION"]
old-location: dshow\dvd_region.htm
tech.root: dshow
ms.assetid: 2a555f98-5037-4a99-a1b7-bea36527309b
ms.date: 12/05/2018
ms.keywords: '*PDVD_REGION, DVD_REGION, DVD_REGION structure [DirectShow], DVD_REGIONStructure, PDVD_REGION, PDVD_REGION structure pointer [DirectShow], dshow.dvd_region, dvdmedia/DVD_REGION, dvdmedia/PDVD_REGION'
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
req.typenames: DVD_REGION, *PDVD_REGION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DVD_REGION
 - dvdmedia/_DVD_REGION
 - PDVD_REGION
 - dvdmedia/PDVD_REGION
 - DVD_REGION
 - dvdmedia/DVD_REGION
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
 - DVD_REGION
---

## -description

Identifies the DVD region as reported by the local system components.

## -struct-fields

### -field CopySystem

Specifies whether the disk is copy protected.

### -field RegionData

Contains information about the region from the decoder.

### -field SystemRegion

Contains information about region from DVD drive.

### -field ResetCount

Reserved.

## -remarks

The AM_PROPERTY_DVDCOPY_REGION property uses this structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>