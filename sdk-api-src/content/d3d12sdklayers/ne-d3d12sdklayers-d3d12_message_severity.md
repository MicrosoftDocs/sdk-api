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

# D3D12_MESSAGE_SEVERITY enumeration


## -description



        Debug message severity levels for an information queue.


## -enum-fields




### -field D3D12_MESSAGE_SEVERITY_CORRUPTION


            Indicates a corruption error.
          


### -field D3D12_MESSAGE_SEVERITY_ERROR


            Indicates an error.
          


### -field D3D12_MESSAGE_SEVERITY_WARNING


            Indicates a warning.
          


### -field D3D12_MESSAGE_SEVERITY_INFO


            Indicates an information message.
          


### -field D3D12_MESSAGE_SEVERITY_MESSAGE


            Indicates a message other than corruption, error, warning or information.
          


## -remarks




          Use these values to allow or deny message categories to pass through the storage and retrieval filters for an information queue (see <a href="https://msdn.microsoft.com/5CD64E71-8530-43FB-B441-25C61ED6F317">D3D12_INFO_QUEUE_FILTER</a>). This API is used by <a href="https://msdn.microsoft.com/C5979BF4-C44D-461F-8FAB-D0577691C5BF">AddApplicationMessage</a> and <a href="https://msdn.microsoft.com/34AAF9BB-5340-4DB3-87B9-6C26AB6C881C">AddMessage</a>.


        




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>
 

 

