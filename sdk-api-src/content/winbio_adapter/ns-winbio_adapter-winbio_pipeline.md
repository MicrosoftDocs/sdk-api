---
UID: NS:winbio_adapter._WINBIO_PIPELINE
title: WINBIO_PIPELINE
author: windows-sdk-content
description: Contains shared context information used by the sensor, engine, and storage adapter components in a single biometric unit.
old-location: secbiomet\winbio_pipeline.htm
tech.root: SecBioMet
ms.assetid: b5fc2b14-b0b6-4327-a42a-ecae41c3e12a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWINBIO_PIPELINE, PWINBIO_PIPELINE, PWINBIO_PIPELINE structure pointer [Windows Biometric Framework API], WINBIO_PIPELINE, WINBIO_PIPELINE structure [Windows Biometric Framework API], secbiomet.winbio_pipeline, winbio_adapter/PWINBIO_PIPELINE, winbio_adapter/WINBIO_PIPELINE"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_PIPELINE
product: Windows
targetos: Windows
req.typenames: WINBIO_PIPELINE, *PWINBIO_PIPELINE
req.redist: 
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

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd401660(v=VS.85).aspx">WINBIO_SENSOR_INTERFACE</a> structure for the biometric unit. Adapters should ignore this field.



### -field EngineInterface

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd401655(v=VS.85).aspx">WINBIO_ENGINE_INTERFACE</a> structure for the biometric unit. Adapters should ignore this field.



### -field StorageInterface

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Dd401661(v=VS.85).aspx">WINBIO_STORAGE_INTERFACE</a> structure for the biometric unit. Adapters should ignore this field.



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




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>
 

 

