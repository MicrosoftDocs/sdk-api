---
UID: NF:baseaudioprocessingobject.AERT_Allocate
title: AERT_Allocate function (baseaudioprocessingobject.h)
description: The AERT_Allocate utility function allocates and locks a segment of memory for use by audio processing objects.
helpviewer_keywords: ["AERT_Allocate","AERT_Allocate function [Audio Devices]","audio.aert_allocate","audio_syseffects_r_db01d2ca-9a2d-4054-b066-773f2cb54276.xml","baseaudioprocessingobject/AERT_Allocate"]
old-location: audio\aert_allocate.htm
tech.root: audio
ms.assetid: b992842d-0612-464c-9b82-b75137fa49eb
ms.date: 12/05/2018
ms.keywords: AERT_Allocate, AERT_Allocate function [Audio Devices], audio.aert_allocate, audio_syseffects_r_db01d2ca-9a2d-4054-b066-773f2cb54276.xml, baseaudioprocessingobject/AERT_Allocate
req.header: baseaudioprocessingobject.h
req.include-header: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating system.
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
req.lib: Audioeng.lib
req.dll: Audioeng.dll
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AERT_Allocate
 - baseaudioprocessingobject/AERT_Allocate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Audioeng.dll
api_name:
 - AERT_Allocate
---

# AERT_Allocate function


## -description

The <code>AERT_Allocate</code> utility function allocates and locks a segment of memory for use by audio processing objects.

## -parameters

### -param size

The number of bytes to allocate.

### -param pMemory

A pointer to the allocated memory.

## -returns

If the function successfully allocates the requested locked memory, the function returns a value of S_OK. The function returns a value of E_OUTOFMEMORY if it cannot find enough memory to allocate and lock.

## -remarks

None

