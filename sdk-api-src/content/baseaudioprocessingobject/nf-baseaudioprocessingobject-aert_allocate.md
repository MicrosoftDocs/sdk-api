---
UID: NF:baseaudioprocessingobject.AERT_Allocate
title: AERT_Allocate function
author: windows-driver-content
description: The AERT_Allocate utility function allocates and locks a segment of memory for use by audio processing objects.
old-location: audio\aert_allocate.htm
old-project: audio
ms.assetid: b992842d-0612-464c-9b82-b75137fa49eb
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: AERT_Allocate, AERT_Allocate function [Audio Devices], audio.aert_allocate, audio_syseffects_r_db01d2ca-9a2d-4054-b066-773f2cb54276.xml, baseaudioprocessingobject/AERT_Allocate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AZ_PROP_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Audioeng.dll
api_name:
-	AERT_Allocate
product: Windows
targetos: Windows
req.lib: Audioeng.lib
req.dll: Audioeng.dll
req.irql: All levels
---

# AERT_Allocate function


## -description


The <code>AERT_Allocate</code> utility function allocates and locks a segment of memory for use by audio processing objects.


## -parameters




### -param size

The number of input connections.


### -param pMemory

A pointer to the allocated memory.


## -returns



If the function successfully allocates the requested locked memory, the function returns a value of S_OK. The function returns a value of E_OUTOFMEMORY if it cannot find enough memory to allocate and lock.




## -remarks



None



