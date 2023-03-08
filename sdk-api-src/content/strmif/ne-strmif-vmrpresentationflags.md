---
UID: NE:strmif.VMRPresentationFlags
title: VMRPresentationFlags (strmif.h)
description: The VMRPresentationFlags enumeration type is a member of the VMRPRESENTATIONINFO structure .
helpviewer_keywords: ["VMRPresentationFlags","VMRPresentationFlags enumeration [DirectShow]","VMRPresentationFlagsEnumeration","VMRSample_Discontinuity","VMRSample_Preroll","VMRSample_SyncPoint","VMRSample_TimeValid","dshow.vmrpresentationflags","strmif/VMRPresentationFlags","strmif/VMRSample_Discontinuity","strmif/VMRSample_Preroll","strmif/VMRSample_SyncPoint","strmif/VMRSample_TimeValid"]
old-location: dshow\vmrpresentationflags.htm
tech.root: dshow
ms.assetid: 27aab657-802e-4967-a5bd-3907637e1cfe
ms.date: 12/05/2018
ms.keywords: VMRPresentationFlags, VMRPresentationFlags enumeration [DirectShow], VMRPresentationFlagsEnumeration, VMRSample_Discontinuity, VMRSample_Preroll, VMRSample_SyncPoint, VMRSample_TimeValid, dshow.vmrpresentationflags, strmif/VMRPresentationFlags, strmif/VMRSample_Discontinuity, strmif/VMRSample_Preroll, strmif/VMRSample_SyncPoint, strmif/VMRSample_TimeValid
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VMRPresentationFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VMRPresentationFlags
 - strmif/VMRPresentationFlags
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
 - VMRPresentationFlags
---

# VMRPresentationFlags enumeration


## -description

The [VMRPRESENTATIONINFO](/windows/desktop/api/strmif/ns-strmif-vmrpresentationinfo) structure .

## -enum-fields

### -field VMRSample_SyncPoint:0x1

Indicates that the sample is a sync point.

### -field VMRSample_Preroll:0x2

Indicates that the sample is part of the preroll.

### -field VMRSample_Discontinuity:0x4

Indicates that the sample is a discontinuity.

### -field VMRSample_TimeValid:0x8

Indicates that the time stamp on the sample is valid.

### -field VMRSample_SrcDstRectsValid:0x10

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
