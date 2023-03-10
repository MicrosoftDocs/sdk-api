---
UID: NS:dvdmedia._AM_DVDCOPY_DISCKEY
title: AM_DVDCOPY_DISCKEY (dvdmedia.h)
description: Specifies the DVD disc key.
helpviewer_keywords: ["*PAM_DVDCOPY_DISCKEY","AM_DVDCOPY_DISCKEY","AM_DVDCOPY_DISCKEY structure [DirectShow]","PAM_DVDCOPY_DISCKEY","PAM_DVDCOPY_DISCKEY structure pointer [DirectShow]","dshow.am_dvdcopy_disckey","dvdmedia/AM_DVDCOPY_DISCKEY","dvdmedia/PAM_DVDCOPY_DISCKEY"]
old-location: dshow\am_dvdcopy_disckey.htm
tech.root: dshow
ms.assetid: ab4d7b2d-59a6-4ad1-9120-552747b96596
ms.date: 12/05/2018
ms.keywords: '*PAM_DVDCOPY_DISCKEY, AM_DVDCOPY_DISCKEY, AM_DVDCOPY_DISCKEY structure [DirectShow], PAM_DVDCOPY_DISCKEY, PAM_DVDCOPY_DISCKEY structure pointer [DirectShow], dshow.am_dvdcopy_disckey, dvdmedia/AM_DVDCOPY_DISCKEY, dvdmedia/PAM_DVDCOPY_DISCKEY'
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
req.typenames: AM_DVDCOPY_DISCKEY, *PAM_DVDCOPY_DISCKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_DVDCOPY_DISCKEY
 - dvdmedia/_AM_DVDCOPY_DISCKEY
 - PAM_DVDCOPY_DISCKEY
 - dvdmedia/PAM_DVDCOPY_DISCKEY
 - AM_DVDCOPY_DISCKEY
 - dvdmedia/AM_DVDCOPY_DISCKEY
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
 - AM_DVDCOPY_DISCKEY
---

# AM_DVDCOPY_DISCKEY structure


## -description

Specifies the DVD disc key.

## -struct-fields

### -field DiscKey

DVD disc key.

## -remarks

The AM_PROPERTY_DVDCOPY_DISC_KEY property uses this structure.

A disc key is used for the DVD CSS key exchange for decryption. Implementors should get a CSS license and further instructions from CSS.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-copy-protection-property-set">DVD Copy Protection Property Set</a>