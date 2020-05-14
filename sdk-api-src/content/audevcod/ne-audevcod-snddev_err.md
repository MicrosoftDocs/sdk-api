---
UID: NE:audevcod._tagSND_DEVICE_ERROR
title: SNDDEV_ERR (audevcod.h)
description: Specifies how the audio device was being accessed when the failure occurred.helpviewer_keywords: ["SNDDEV_ERR","SNDDEV_ERR","SNDDEV_ERR enumeration [DirectShow]","SNDDEV_ERREnumeration","SNDDEV_ERROR_AddBuffer","SNDDEV_ERROR_Close","SNDDEV_ERROR_GetCaps","SNDDEV_ERROR_GetPosition","SNDDEV_ERROR_Open","SNDDEV_ERROR_Pause","SNDDEV_ERROR_PrepareHeader","SNDDEV_ERROR_Query","SNDDEV_ERROR_Reset","SNDDEV_ERROR_Restart","SNDDEV_ERROR_Start","SNDDEV_ERROR_Stop","SNDDEV_ERROR_UnprepareHeader","SNDDEV_ERROR_Write","audevcod/SNDDEV_ERR","audevcod/SNDDEV_ERROR_AddBuffer","audevcod/SNDDEV_ERROR_Close","audevcod/SNDDEV_ERROR_GetCaps","audevcod/SNDDEV_ERROR_GetPosition","audevcod/SNDDEV_ERROR_Open","audevcod/SNDDEV_ERROR_Pause","audevcod/SNDDEV_ERROR_PrepareHeader","audevcod/SNDDEV_ERROR_Query","audevcod/SNDDEV_ERROR_Reset","audevcod/SNDDEV_ERROR_Restart","audevcod/SNDDEV_ERROR_Start","audevcod/SNDDEV_ERROR_Stop","audevcod/SNDDEV_ERROR_UnprepareHeader","audevcod/SNDDEV_ERROR_Write","dshow.snddev_err"]
old-location: dshow\snddev_err.htm
tech.root: DirectShow
ms.assetid: 0a3def41-e3b4-416f-ad64-16394bd234c2
ms.date: 12/05/2018
ms.keywords: SNDDEV_ERR, SNDDEV_ERR , SNDDEV_ERR enumeration [DirectShow], SNDDEV_ERREnumeration, SNDDEV_ERROR_AddBuffer, SNDDEV_ERROR_Close, SNDDEV_ERROR_GetCaps, SNDDEV_ERROR_GetPosition, SNDDEV_ERROR_Open, SNDDEV_ERROR_Pause, SNDDEV_ERROR_PrepareHeader, SNDDEV_ERROR_Query, SNDDEV_ERROR_Reset, SNDDEV_ERROR_Restart, SNDDEV_ERROR_Start, SNDDEV_ERROR_Stop, SNDDEV_ERROR_UnprepareHeader, SNDDEV_ERROR_Write, audevcod/SNDDEV_ERR, audevcod/SNDDEV_ERROR_AddBuffer, audevcod/SNDDEV_ERROR_Close, audevcod/SNDDEV_ERROR_GetCaps, audevcod/SNDDEV_ERROR_GetPosition, audevcod/SNDDEV_ERROR_Open, audevcod/SNDDEV_ERROR_Pause, audevcod/SNDDEV_ERROR_PrepareHeader, audevcod/SNDDEV_ERROR_Query, audevcod/SNDDEV_ERROR_Reset, audevcod/SNDDEV_ERROR_Restart, audevcod/SNDDEV_ERROR_Start, audevcod/SNDDEV_ERROR_Stop, audevcod/SNDDEV_ERROR_UnprepareHeader, audevcod/SNDDEV_ERROR_Write, dshow.snddev_err
f1_keywords:
- audevcod/SNDDEV_ERR
dev_langs:
- c++
req.header: audevcod.h
req.include-header: Dshow.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- audevcod.h
api_name:
- SNDDEV_ERR
targetos: Windows
req.typenames: SNDDEV_ERR
req.redist: 
ms.custom: 19H1
---

# SNDDEV_ERR enumeration


## -description



Specifies how the audio device was being accessed when the failure occurred.




## -enum-fields




### -field SNDDEV_ERROR_Open

The audio device attempted to open.
          


### -field SNDDEV_ERROR_Close

The audio device attempted to close.
          


### -field SNDDEV_ERROR_GetCaps

The capabilities of the underlying hardware were being retrieved.
          


### -field SNDDEV_ERROR_PrepareHeader

The header for the audio device was being prepared.
          


### -field SNDDEV_ERROR_UnprepareHeader

The header for the audio device was being unprepared.
          


### -field SNDDEV_ERROR_Reset

The audio device attempted to reset.
          


### -field SNDDEV_ERROR_Restart

The audio device attempted to restart.
          


### -field SNDDEV_ERROR_GetPosition

The current and stop position settings were being retrieved.
          


### -field SNDDEV_ERROR_Write

The audio device was being written to.
          


### -field SNDDEV_ERROR_Pause

The audio device attempted to pause.
          


### -field SNDDEV_ERROR_Stop

The audio device attempted to stop.
          


### -field SNDDEV_ERROR_Start

The audio device attempted to start.
          


### -field SNDDEV_ERROR_AddBuffer

A buffer was being added to the audio device.
          


### -field SNDDEV_ERROR_Query

The audio device was being queried.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
 

 

