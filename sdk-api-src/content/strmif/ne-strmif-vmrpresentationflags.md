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
f1_keywords:
- strmif/VMRPresentationFlags
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- strmif.h
api_name:
- VMRPresentationFlags
targetos: Windows
req.typenames: VMRPresentationFlags
req.redist: 
ms.custom: 19H1
---

# VMRPresentationFlags enumeration


## -description



The [VMRPRESENTATIONINFO](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-vmrpresentationinfo) structure .




## -enum-fields




### -field VMRSample_SyncPoint

Indicates that the sample is a sync point.
          


### -field VMRSample_Preroll

Indicates that the sample is part of the preroll.
          


### -field VMRSample_Discontinuity

Indicates that the sample is a discontinuity.
          


### -field VMRSample_TimeValid

Indicates that the time stamp on the sample is valid.
          


### -field VMRSample_SrcDstRectsValid




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
 

 

