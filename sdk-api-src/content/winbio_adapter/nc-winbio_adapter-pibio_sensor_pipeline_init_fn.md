---
UID: NC:winbio_adapter.PIBIO_SENSOR_PIPELINE_INIT_FN
title: PIBIO_SENSOR_PIPELINE_INIT_FN
author: windows-sdk-content
description: Gives the Sensor Adapter the chance to perform any initialization that remains incomplete, and which requires help from the Engine or Storage adapter components.
old-location: secbiomet\sensoradapterpipelineinit.htm
old-project: secbiomet
ms.assetid: 91667505-78D6-405E-9028-DF4F3037B455
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: PIBIO_SENSOR_PIPELINE_INIT_FN, PIBIO_SENSOR_PIPELINE_INIT_FN callback, SensorAdapterPipelineInit, SensorAdapterPipelineInit callback function [Windows Biometric Framework API], secbiomet.sensoradapterpipelineinit, winbio_adapter/SensorAdapterPipelineInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - SensorAdapterPipelineInit
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_PIPELINE_INIT_FN callback function


## -description


Called by the Windows Biometric Framework to give the Sensor Adapter the chance to perform any initialization that remains incomplete, and which requires help from the Engine or Storage adapter components.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Any error code will cause the Biometric Service to log the error and abort the configuration of the biometric unit.

</td>
</tr>
</table>
 




## -remarks



The Sensor Adapter should return <b>S_OK</b> if it doesn’t need to perform any initialization at this point.

When this routine is called, the <a href="https://msdn.microsoft.com/e797952b-c7dd-41ad-9536-97d7ce1a7a5d">EngineAdapterAttach</a>, <a href="https://msdn.microsoft.com/6abded6b-12e0-4cc6-a011-0b18e8ea747b">StorageAdapterAttach</a>, <a href="https://msdn.microsoft.com/69D4BB35-2E00-4FF6-8A69-DFCEFA5785A0">EngineAdapterPipelineInit</a>, and <a href="https://msdn.microsoft.com/F969AC5A-6760-4904-A04E-F2FEF4290F7A">StorageAdapterPipelineInit</a> routines have completed normally.

This method executes in the context of an arbitrary RPC server thread.



