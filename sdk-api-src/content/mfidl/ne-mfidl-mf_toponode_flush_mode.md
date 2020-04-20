---
UID: NE:mfidl._MF_TOPONODE_FLUSH_MODE
title: MF_TOPONODE_FLUSH_MODE (mfidl.h)
description: Defines when a transform in a topology is flushed.helpviewer_keywords: ["MF_TOPONODE_FLUSH_ALWAYS","MF_TOPONODE_FLUSH_MODE","MF_TOPONODE_FLUSH_MODE enumeration [Media Foundation]","MF_TOPONODE_FLUSH_NEVER","MF_TOPONODE_FLUSH_SEEK","e7eec3c1-f4be-4d7f-9d4c-e98a6a05e85a","mf.mf_toponode_flush_mode","mfidl/MF_TOPONODE_FLUSH_ALWAYS","mfidl/MF_TOPONODE_FLUSH_MODE","mfidl/MF_TOPONODE_FLUSH_NEVER","mfidl/MF_TOPONODE_FLUSH_SEEK"]
old-location: mf\mf_toponode_flush_mode.htm
tech.root: medfound
ms.assetid: e7eec3c1-f4be-4d7f-9d4c-e98a6a05e85a
ms.date: 12/05/2018
ms.keywords: MF_TOPONODE_FLUSH_ALWAYS, MF_TOPONODE_FLUSH_MODE, MF_TOPONODE_FLUSH_MODE enumeration [Media Foundation], MF_TOPONODE_FLUSH_NEVER, MF_TOPONODE_FLUSH_SEEK, e7eec3c1-f4be-4d7f-9d4c-e98a6a05e85a, mf.mf_toponode_flush_mode, mfidl/MF_TOPONODE_FLUSH_ALWAYS, mfidl/MF_TOPONODE_FLUSH_MODE, mfidl/MF_TOPONODE_FLUSH_NEVER, mfidl/MF_TOPONODE_FLUSH_SEEK
f1_keywords:
- mfidl/MF_TOPONODE_FLUSH_MODE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mfidl.h
api_name:
- MF_TOPONODE_FLUSH_MODE
targetos: Windows
req.typenames: MF_TOPONODE_FLUSH_MODE
req.redist: 
ms.custom: 19H1
---

# MF_TOPONODE_FLUSH_MODE enumeration


## -description



Defines when a transform in a topology is flushed.




## -enum-fields




### -field MF_TOPONODE_FLUSH_ALWAYS

The transform is flushed whenever the stream changes, including seeks and new segments.


### -field MF_TOPONODE_FLUSH_SEEK

The transform is flushed when seeking is performed on the stream.


### -field MF_TOPONODE_FLUSH_NEVER

The transform is never flushed during streaming. It is flushed only when the object is released.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/mf-toponode-flush-attribute">MF_TOPONODE_FLUSH</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

