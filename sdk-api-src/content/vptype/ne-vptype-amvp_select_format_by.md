---
UID: NE:vptype._AMVP_SELECT_FORMAT_BY
title: AMVP_SELECT_FORMAT_BY (vptype.h)
description: Specifies the criteria that the Overlay Mixer Filter should use to select the video format.
helpviewer_keywords: ["AMVP_BEST_BANDWIDTH","AMVP_DO_NOT_CARE","AMVP_INPUT_SAME_AS_OUTPUT","AMVP_SELECT_FORMAT_BY","AMVP_SELECT_FORMAT_BY","AMVP_SELECT_FORMAT_BY enumeration [DirectShow]","AMVP_SELECT_FORMAT_BYEnumeration","dshow.amvp_select_format_by","vptype/AMVP_BEST_BANDWIDTH","vptype/AMVP_DO_NOT_CARE","vptype/AMVP_INPUT_SAME_AS_OUTPUT","vptype/AMVP_SELECT_FORMAT_BY"]
old-location: dshow\amvp_select_format_by.htm
tech.root: dshow
ms.assetid: 98f60199-630b-4759-a0fa-86292713a36d
ms.date: 12/05/2018
ms.keywords: AMVP_BEST_BANDWIDTH, AMVP_DO_NOT_CARE, AMVP_INPUT_SAME_AS_OUTPUT, AMVP_SELECT_FORMAT_BY, AMVP_SELECT_FORMAT_BY , AMVP_SELECT_FORMAT_BY enumeration [DirectShow], AMVP_SELECT_FORMAT_BYEnumeration, dshow.amvp_select_format_by, vptype/AMVP_BEST_BANDWIDTH, vptype/AMVP_DO_NOT_CARE, vptype/AMVP_INPUT_SAME_AS_OUTPUT, vptype/AMVP_SELECT_FORMAT_BY
req.header: vptype.h
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
req.typenames: AMVP_SELECT_FORMAT_BY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMVP_SELECT_FORMAT_BY
 - vptype/_AMVP_SELECT_FORMAT_BY
 - AMVP_SELECT_FORMAT_BY
 - vptype/AMVP_SELECT_FORMAT_BY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - vptype.h
api_name:
 - AMVP_SELECT_FORMAT_BY
---

# AMVP_SELECT_FORMAT_BY enumeration


## -description

Specifies the criteria that the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a> should use to select the video format.

## -enum-fields

### -field AMVP_DO_NOT_CARE

Format does not matter.

### -field AMVP_BEST_BANDWIDTH

Use the largest bandwidth.

### -field AMVP_INPUT_SAME_AS_OUTPUT

Use the same input format as output format.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>