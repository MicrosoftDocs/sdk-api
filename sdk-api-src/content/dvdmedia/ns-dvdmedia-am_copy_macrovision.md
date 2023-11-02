---
UID: NS:dvdmedia._AM_COPY_MACROVISION
title: AM_COPY_MACROVISION (dvdmedia.h)
description: The AM_COPY_MACROVISION structure specifies the analog copy protection level for an NTSC encoder.
helpviewer_keywords: ["*PAM_COPY_MACROVISION","AM_COPY_MACROVISION","AM_COPY_MACROVISION structure [DirectShow]","PAM_COPY_MACROVISION","PAM_COPY_MACROVISION structure pointer [DirectShow]","dshow.am_copy_macrovision","dvdmedia/AM_COPY_MACROVISION","dvdmedia/PAM_COPY_MACROVISION"]
old-location: dshow\am_copy_macrovision.htm
tech.root: dshow
ms.assetid: 7fb1b12a-92f4-48e2-8ebe-359ebc33cd09
ms.date: 12/05/2018
ms.keywords: '*PAM_COPY_MACROVISION, AM_COPY_MACROVISION, AM_COPY_MACROVISION structure [DirectShow], PAM_COPY_MACROVISION, PAM_COPY_MACROVISION structure pointer [DirectShow], dshow.am_copy_macrovision, dvdmedia/AM_COPY_MACROVISION, dvdmedia/PAM_COPY_MACROVISION'
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
req.typenames: AM_COPY_MACROVISION, *PAM_COPY_MACROVISION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_COPY_MACROVISION
 - dvdmedia/_AM_COPY_MACROVISION
 - PAM_COPY_MACROVISION
 - dvdmedia/PAM_COPY_MACROVISION
 - AM_COPY_MACROVISION
 - dvdmedia/AM_COPY_MACROVISION
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
 - AM_COPY_MACROVISION
---

# AM_COPY_MACROVISION structure


## -description

The <b>AM_COPY_MACROVISION</b> structure specifies the analog copy protection level for an NTSC encoder.

## -struct-fields

### -field MACROVISIONLevel

Analog copy protection level for the NTSC encoder. Member of the <a href="/previous-versions/ms778997(v=vs.85)">AM_COPY_MACROVISION_LEVEL</a> enumerated data type.

## -remarks

The AM_PROPERTY_COPY_MACROVISION property of the <a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection</a> property set uses this structure.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>