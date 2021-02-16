---
UID: NS:winbio_adapter._WINBIO_PIPELINE
title: WINBIO_PIPELINE (winbio_adapter.h)
description: Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.
helpviewer_keywords: ["*PWINBIO_PIPELINE","PWINBIO_PIPELINE","PWINBIO_PIPELINE structure pointer [Windows Biometric Framework API]","WINBIO_PIPELINE","WINBIO_PIPELINE structure [Windows Biometric Framework API]","secbiomet.winbio_pipeline","winbio_adapter/PWINBIO_PIPELINE","winbio_adapter/WINBIO_PIPELINE"]
old-location: secbiomet\winbio_pipeline.htm
tech.root: SecBioMet
ms.assetid: b5fc2b14-b0b6-4327-a42a-ecae41c3e12a
ms.date: 12/05/2018
ms.keywords: '*PWINBIO_PIPELINE, PWINBIO_PIPELINE, PWINBIO_PIPELINE structure pointer [Windows Biometric Framework API], WINBIO_PIPELINE, WINBIO_PIPELINE structure [Windows Biometric Framework API], secbiomet.winbio_pipeline, winbio_adapter/PWINBIO_PIPELINE, winbio_adapter/WINBIO_PIPELINE'
req.header: winbio_adapter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WINBIO_PIPELINE, *PWINBIO_PIPELINE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINBIO_PIPELINE
 - winbio_adapter/_WINBIO_PIPELINE
 - PWINBIO_PIPELINE
 - winbio_adapter/PWINBIO_PIPELINE
 - WINBIO_PIPELINE
 - winbio_adapter/WINBIO_PIPELINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_PIPELINE
---

# WINBIO_PIPELINE structure


## -description

The <b>WINBIO_PIPELINE</b> structure contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.

## -struct-fields

### -field SensorHandle

File handle to the sensor device associated with the biometric unit. Adapters should treat this as a read-only field.

### -field EngineHandle

File handle to the dedicated hardware matching engine, if one is present. This is modified only by the engine adapter. It is read by the Windows Biometric Framework.

### -field StorageHandle

File handle to the template storage database. This is read by the Windows Biometric Framework, but it is modified only by the storage adapter.

### -field SensorInterface

Pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_sensor_interface">WINBIO_SENSOR_INTERFACE</a> structure for the biometric unit. Adapters should ignore this field.

### -field EngineInterface

Pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_engine_interface">WINBIO_ENGINE_INTERFACE</a> structure for the biometric unit. Adapters should ignore this field.

### -field StorageInterface

Pointer to the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a> structure for the biometric unit. Adapters should ignore this field.

### -field SensorContext

Pointer to a private data structure defined by the sensor adapter. This pointer and the structure contents are managed by the sensor adapter and are never accessed by the Windows Biometric Framework.

### -field EngineContext

Pointer to a private data structure defined by the engine adapter. This pointer and the structure contents are managed by the engine adapter and are never accessed by the Windows Biometric Framework.

### -field StorageContext

Pointer to a private data structure defined by the storage adapter. This pointer and the structure contents are managed by the storage adapter and are never accessed by the Windows Biometric Framework.

### -field FrameworkInterface

## -remarks

Each biometric unit has its own unique <b>WINBIO_PIPELINE</b> structure to maintain the current processing state of operations performed by the biometric unit. The Windows Biometric Framework automatically passes the address of the pipeline structure to each adapter in the component stack. Adapters use this pipeline pointer to access their own private context data and to call functions in lower levels of the component stack.

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/SecBioMet/plug-in-structures">Plug-in Structures</a>