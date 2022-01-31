---
UID: NE:mfidl._MF_TOPONODE_DRAIN_MODE
title: MF_TOPONODE_DRAIN_MODE (mfidl.h)
description: Defines at what times a transform in a topology is drained.
helpviewer_keywords: ["7f84fd12-40c3-4201-8986-a2883ba2f53d","MF_TOPONODE_DRAIN_ALWAYS","MF_TOPONODE_DRAIN_DEFAULT","MF_TOPONODE_DRAIN_MODE","MF_TOPONODE_DRAIN_MODE enumeration [Media Foundation]","MF_TOPONODE_DRAIN_NEVER","mf.mf_toponode_drain_mode","mfidl/MF_TOPONODE_DRAIN_ALWAYS","mfidl/MF_TOPONODE_DRAIN_DEFAULT","mfidl/MF_TOPONODE_DRAIN_MODE","mfidl/MF_TOPONODE_DRAIN_NEVER"]
old-location: mf\mf_toponode_drain_mode.htm
tech.root: mf
ms.assetid: 7f84fd12-40c3-4201-8986-a2883ba2f53d
ms.date: 12/05/2018
ms.keywords: 7f84fd12-40c3-4201-8986-a2883ba2f53d, MF_TOPONODE_DRAIN_ALWAYS, MF_TOPONODE_DRAIN_DEFAULT, MF_TOPONODE_DRAIN_MODE, MF_TOPONODE_DRAIN_MODE enumeration [Media Foundation], MF_TOPONODE_DRAIN_NEVER, mf.mf_toponode_drain_mode, mfidl/MF_TOPONODE_DRAIN_ALWAYS, mfidl/MF_TOPONODE_DRAIN_DEFAULT, mfidl/MF_TOPONODE_DRAIN_MODE, mfidl/MF_TOPONODE_DRAIN_NEVER
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
req.typenames: MF_TOPONODE_DRAIN_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_TOPONODE_DRAIN_MODE
 - mfidl/_MF_TOPONODE_DRAIN_MODE
 - MF_TOPONODE_DRAIN_MODE
 - mfidl/MF_TOPONODE_DRAIN_MODE
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
 - MF_TOPONODE_DRAIN_MODE
---

# MF_TOPONODE_DRAIN_MODE enumeration


## -description

Defines at what times a transform in a topology is drained.

## -enum-fields

### -field MF_TOPONODE_DRAIN_DEFAULT:0

The transform is drained when the end of a stream is reached. It is not drained when markout is reached at the end of a segment.

### -field MF_TOPONODE_DRAIN_ALWAYS

The transform is drained whenever a topology ends.

### -field MF_TOPONODE_DRAIN_NEVER

The transform is never drained.

## -see-also

<a href="/windows/desktop/medfound/mf-toponode-drain-attribute">MF_TOPONODE_DRAIN</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
