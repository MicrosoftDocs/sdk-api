---
UID: NE:mfobjects._MF2DBuffer_LockFlags
title: MF2DBuffer_LockFlags (mfobjects.h)
description: Contains flags for the IMF2DBuffer2::Lock2DSize method.
helpviewer_keywords: ["MF2DBuffer_LockFlags","MF2DBuffer_LockFlags enumeration [Media Foundation]","MF2DBuffer_LockFlags_ForceDWORD","MF2DBuffer_LockFlags_LockTypeMask","MF2DBuffer_LockFlags_Read","MF2DBuffer_LockFlags_ReadWrite","MF2DBuffer_LockFlags_Write","mf.mf2dbuffer_lockflags","mfobjects/MF2DBuffer_LockFlags","mfobjects/MF2DBuffer_LockFlags_ForceDWORD","mfobjects/MF2DBuffer_LockFlags_LockTypeMask","mfobjects/MF2DBuffer_LockFlags_Read","mfobjects/MF2DBuffer_LockFlags_ReadWrite","mfobjects/MF2DBuffer_LockFlags_Write"]
old-location: mf\mf2dbuffer_lockflags.htm
tech.root: mf
ms.assetid: 298E3FBE-1902-4AA1-9CC8-5B8D65A48ECF
ms.date: 12/05/2018
ms.keywords: MF2DBuffer_LockFlags, MF2DBuffer_LockFlags enumeration [Media Foundation], MF2DBuffer_LockFlags_ForceDWORD, MF2DBuffer_LockFlags_LockTypeMask, MF2DBuffer_LockFlags_Read, MF2DBuffer_LockFlags_ReadWrite, MF2DBuffer_LockFlags_Write, mf.mf2dbuffer_lockflags, mfobjects/MF2DBuffer_LockFlags, mfobjects/MF2DBuffer_LockFlags_ForceDWORD, mfobjects/MF2DBuffer_LockFlags_LockTypeMask, mfobjects/MF2DBuffer_LockFlags_Read, mfobjects/MF2DBuffer_LockFlags_ReadWrite, mfobjects/MF2DBuffer_LockFlags_Write
req.header: mfobjects.h
req.include-header: Mfobjects.h, Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: MF2DBuffer_LockFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF2DBuffer_LockFlags
 - mfobjects/_MF2DBuffer_LockFlags
 - MF2DBuffer_LockFlags
 - mfobjects/MF2DBuffer_LockFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.idl
api_name:
 - MF2DBuffer_LockFlags
---

# MF2DBuffer_LockFlags enumeration


## -description

Contains flags for the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer2-lock2dsize">IMF2DBuffer2::Lock2DSize</a> method.

## -enum-fields

### -field MF2DBuffer_LockFlags_LockTypeMask

Reserved.

### -field MF2DBuffer_LockFlags_Read:0x1

Lock the buffer for reading.

### -field MF2DBuffer_LockFlags_Write:0x2

Lock the buffer for writing.

### -field MF2DBuffer_LockFlags_ReadWrite:0x3

Lock the buffer for both reading and writing.

### -field MF2DBuffer_LockFlags_ForceDWORD:0x7fffffff

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
