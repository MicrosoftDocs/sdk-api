---
UID: NS:dvdmedia.AM_DVDCOPY_TITLEKEY
title: AM_DVDCOPY_TITLEKEY (dvdmedia.h)
description: Specifies the DVD title key from the current content.
helpviewer_keywords: ["*PAM_DVDCOPY_TITLEKEY","AM_DVDCOPY_TITLEKEY","AM_DVDCOPY_TITLEKEY structure [DirectShow]","PAM_DVDCOPY_TITLEKEY","PAM_DVDCOPY_TITLEKEY structure pointer [DirectShow]","dshow.am_dvdcopy_titlekey","dvdmedia/AM_DVDCOPY_TITLEKEY","dvdmedia/PAM_DVDCOPY_TITLEKEY"]
old-location: dshow\am_dvdcopy_titlekey.htm
tech.root: dshow
ms.assetid: 14460ad8-4c7b-4566-b1ac-9a35fd20f3f3
ms.date: 12/05/2018
ms.keywords: '*PAM_DVDCOPY_TITLEKEY, AM_DVDCOPY_TITLEKEY, AM_DVDCOPY_TITLEKEY structure [DirectShow], PAM_DVDCOPY_TITLEKEY, PAM_DVDCOPY_TITLEKEY structure pointer [DirectShow], dshow.am_dvdcopy_titlekey, dvdmedia/AM_DVDCOPY_TITLEKEY, dvdmedia/PAM_DVDCOPY_TITLEKEY'
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
req.typenames: AM_DVDCOPY_TITLEKEY, *PAM_DVDCOPY_TITLEKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_DVDCOPY_TITLEKEY
 - dvdmedia/AM_DVDCOPY_TITLEKEY
 - PAM_DVDCOPY_TITLEKEY
 - dvdmedia/PAM_DVDCOPY_TITLEKEY
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
 - AM_DVDCOPY_TITLEKEY
---

## -description

Specifies the DVD title key from the current content.

## -struct-fields

### -field KeyFlags

Key flags.

### -field TitleKey

Title key.

### -field Reserved

Reserved.
 
## -remarks

The AM_PROPERTY_DVDCOPY_TITLE_KEY property uses this structure.

A title key is used for the DVD CSS key exchange for decryption. Implementors should get a CSS license and further instructions from CSS.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>