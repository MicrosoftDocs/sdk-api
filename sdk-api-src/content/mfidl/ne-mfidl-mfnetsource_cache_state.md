---
UID: NE:mfidl._MFNETSOURCE_CACHE_STATE
title: MFNETSOURCE_CACHE_STATE (mfidl.h)
description: Defines the status of the cache for a media file or entry.
helpviewer_keywords: ["MFNETSOURCE_CACHE_ACTIVE_COMPLETE","MFNETSOURCE_CACHE_ACTIVE_WRITING","MFNETSOURCE_CACHE_STATE","MFNETSOURCE_CACHE_STATE enumeration [Media Foundation]","MFNETSOURCE_CACHE_UNAVAILABLE","fc7f2f66-02a3-455a-820b-304a53494ef1","mf.mfnetsource_cache_state","mfidl/MFNETSOURCE_CACHE_ACTIVE_COMPLETE","mfidl/MFNETSOURCE_CACHE_ACTIVE_WRITING","mfidl/MFNETSOURCE_CACHE_STATE","mfidl/MFNETSOURCE_CACHE_UNAVAILABLE"]
old-location: mf\mfnetsource_cache_state.htm
tech.root: mf
ms.assetid: fc7f2f66-02a3-455a-820b-304a53494ef1
ms.date: 12/05/2018
ms.keywords: MFNETSOURCE_CACHE_ACTIVE_COMPLETE, MFNETSOURCE_CACHE_ACTIVE_WRITING, MFNETSOURCE_CACHE_STATE, MFNETSOURCE_CACHE_STATE enumeration [Media Foundation], MFNETSOURCE_CACHE_UNAVAILABLE, fc7f2f66-02a3-455a-820b-304a53494ef1, mf.mfnetsource_cache_state, mfidl/MFNETSOURCE_CACHE_ACTIVE_COMPLETE, mfidl/MFNETSOURCE_CACHE_ACTIVE_WRITING, mfidl/MFNETSOURCE_CACHE_STATE, mfidl/MFNETSOURCE_CACHE_UNAVAILABLE
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFNETSOURCE_CACHE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFNETSOURCE_CACHE_STATE
 - mfidl/_MFNETSOURCE_CACHE_STATE
 - MFNETSOURCE_CACHE_STATE
 - mfidl/MFNETSOURCE_CACHE_STATE
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
 - MFNETSOURCE_CACHE_STATE
---

# MFNETSOURCE_CACHE_STATE enumeration


## -description

Defines the status of the cache for a media file or entry.

## -enum-fields

### -field MFNETSOURCE_CACHE_UNAVAILABLE:0

The cache for a file or entry does not exist.

### -field MFNETSOURCE_CACHE_ACTIVE_WRITING

The cache for a file or entry is growing.

### -field MFNETSOURCE_CACHE_ACTIVE_COMPLETE

The cache for a file or entry is completed.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
