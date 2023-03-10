---
UID: NS:vmr9._VMR9PresentationInfo
title: VMR9PresentationInfo (vmr9.h)
description: The VMR9PresentationInfo structure is used with the VMR-9 in the IVMRImagePresenter9::PresentImage method.
helpviewer_keywords: ["VMR9PresentationInfo","VMR9PresentationInfo structure [DirectShow]","VMR9PresentationInfoStructure","dshow.vmr9presentationinfo","vmr9/VMR9PresentationInfo"]
old-location: dshow\vmr9presentationinfo.htm
tech.root: dshow
ms.assetid: 7e5cf0e9-1cb9-494a-9370-550328dcd85c
ms.date: 12/05/2018
ms.keywords: VMR9PresentationInfo, VMR9PresentationInfo structure [DirectShow], VMR9PresentationInfoStructure, dshow.vmr9presentationinfo, vmr9/VMR9PresentationInfo
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
req.typenames: VMR9PresentationInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VMR9PresentationInfo
 - vmr9/_VMR9PresentationInfo
 - VMR9PresentationInfo
 - vmr9/VMR9PresentationInfo
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
 - VMR9PresentationInfo
---

# VMR9PresentationInfo structure


## -description

The <code>VMR9PresentationInfo</code> structure is used with the VMR-9 in the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrimagepresenter9-presentimage">IVMRImagePresenter9::PresentImage</a> method.

## -struct-fields

### -field dwFlags

Contains a bitwise combination of flags from the <a href="/previous-versions/windows/desktop/api/vmr9/ne-vmr9-vmr9presentationflags">VMR9PresentationFlags</a> enumeration type. These flags describe the status of the video sample with respect to its presentation time.

### -field lpSurf

Pointer to the DirectDraw surface that contains the video frame.

### -field rtStart

Specifies the start time for the video frame.

### -field rtEnd

Specifies the end time for the video frame

### -field szAspectRatio

Specifies the aspect ratio of the video, as a <b>SIZE</b> structure.

### -field rcSrc

Specifies the source rectangle.

### -field rcDst

Specifies the destination rectangle.

### -field dwReserved1

Reserved.

### -field dwReserved2

Reserved.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>