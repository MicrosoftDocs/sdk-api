---
UID: NE:mfidl.MFTIMER_FLAGS
title: MFTIMER_FLAGS (mfidl.h)
description: Contains flags for the IMFTimer::SetTimer method.
helpviewer_keywords: ["MFTIMER_FLAGS","MFTIMER_FLAGS enumeration [Media Foundation]","MFTIMER_RELATIVE","bd94247a-ed58-4857-a39d-16880eea75e0","mf.mftimer_flags","mfidl/MFTIMER_FLAGS","mfidl/MFTIMER_RELATIVE"]
old-location: mf\mftimer_flags.htm
tech.root: mf
ms.assetid: bd94247a-ed58-4857-a39d-16880eea75e0
ms.date: 12/05/2018
ms.keywords: MFTIMER_FLAGS, MFTIMER_FLAGS enumeration [Media Foundation], MFTIMER_RELATIVE, bd94247a-ed58-4857-a39d-16880eea75e0, mf.mftimer_flags, mfidl/MFTIMER_FLAGS, mfidl/MFTIMER_RELATIVE
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFTIMER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFTIMER_FLAGS
 - mfidl/MFTIMER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFTIMER_FLAGS
---

# MFTIMER_FLAGS enumeration


## -description

Contains flags for the <a href="/windows/desktop/api/mfidl/nf-mfidl-imftimer-settimer">IMFTimer::SetTimer</a> method.

## -enum-fields

### -field MFTIMER_RELATIVE:0x1

The time passed to the timer is relative to the current time. If this flag is absent, the time is expressed as an absolute clock time.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
