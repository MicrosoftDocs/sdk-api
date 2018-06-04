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

# D3D12_RLDO_FLAGS enumeration


## -description



          Specifies options for the amount of information to report about a live device object's lifetime.


        


## -enum-fields




### -field D3D12_RLDO_NONE


### -field D3D12_RLDO_SUMMARY

Obtain a summary about a live device object's lifetime. 




### -field D3D12_RLDO_DETAIL

Obtain detailed information about a live device object's lifetime. 


          


### -field D3D12_RLDO_IGNORE_INTERNAL


            Internal use only.


## -remarks




          This enumeration is used by <a href="https://msdn.microsoft.com/37771598-DC2E-42FA-B17D-A187164A3314">ID3D12DebugDevice::ReportLiveDeviceObjects</a>. 




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>
 

 

