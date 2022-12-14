---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0000_0002
title: VMR9PresentationFlags (vmr9.h)
description: The VMR9PresentationFlags enumeration type contains flags that describe the status of a video sample. These flags are used in the VMR9PresentationInfo structure.
helpviewer_keywords: ["VMR9PresentationFlags","VMR9PresentationFlags","VMR9PresentationFlags enumeration [DirectShow]","VMR9PresentationFlagsEnumeration","VMR9Sample_Discontinuity","VMR9Sample_Preroll","VMR9Sample_SyncPoint","VMR9Sample_TimeValid","dshow.vmr9presentationflags","enumeration [DirectShow]","vmr9/VMR9PresentationFlags","vmr9/VMR9Sample_Discontinuity","vmr9/VMR9Sample_Preroll","vmr9/VMR9Sample_SyncPoint","vmr9/VMR9Sample_TimeValid"]
old-location: dshow\vmr9presentationflags.htm
tech.root: dshow
ms.assetid: 97db420f-a6a5-4c87-9c7f-9733a1ce2b46
ms.date: 12/05/2018
ms.keywords: VMR9PresentationFlags, VMR9PresentationFlags , VMR9PresentationFlags enumeration [DirectShow], VMR9PresentationFlagsEnumeration, VMR9Sample_Discontinuity, VMR9Sample_Preroll, VMR9Sample_SyncPoint, VMR9Sample_TimeValid, dshow.vmr9presentationflags, enumeration [DirectShow], vmr9/VMR9PresentationFlags, vmr9/VMR9Sample_Discontinuity, vmr9/VMR9Sample_Preroll, vmr9/VMR9Sample_SyncPoint, vmr9/VMR9Sample_TimeValid
req.header: vmr9.h
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
req.typenames: VMR9PresentationFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0000_0002
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0000_0002
 - VMR9PresentationFlags
 - vmr9/VMR9PresentationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9PresentationFlags
---

# VMR9PresentationFlags enumeration


## -description

The <code>VMR9PresentationFlags</code> enumeration type contains flags that describe the status of a video sample. These flags are used in the <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9presentationinfo">VMR9PresentationInfo</a> structure.

## -enum-fields

### -field VMR9Sample_SyncPoint:0x1

Indicates that the sample is a sync point.

### -field VMR9Sample_Preroll:0x2

Indicates that the sample is part of the preroll.

### -field VMR9Sample_Discontinuity:0x4

Indicates that the sample is a discontinuity.

### -field VMR9Sample_TimeValid:0x8

Indicates that the time stamp on the sample is valid.

### -field VMR9Sample_SrcDstRectsValid:0x10

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
