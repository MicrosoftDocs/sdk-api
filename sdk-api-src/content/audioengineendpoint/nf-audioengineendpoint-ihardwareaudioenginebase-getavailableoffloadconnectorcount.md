---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IHardwareAudioEngineBase::GetAvailableOffloadConnectorCount


## -description


The <b>GetAvailableOffloadConnectorCount</b> method retrieves the number of avaialable endpoints that can handle offloaded streams on the hardware audio engine.


## -parameters




### -param _pwstrDeviceId [in]

A pointer to the device ID of the hardware audio engine device.


### -param _uConnectorId [in]

The identifier for the endpoint connector.


### -param _pAvailableConnectorInstanceCount [out]

A pointer to the number of available endpoint connectors that can handle offloaded audio streams.


## -returns



The <b>GetAvailableOffloadConnectorCount</b> method returns <b>S_OK</b> to indicate that it has completed successfully. Otherwise it returns an appropriate error code. 






## -see-also




<a href="https://msdn.microsoft.com/6FB9BEDB-111B-4F0A-B8BB-B0BA2024EB24">IHardwareAudioEngineBase</a>
 

 

