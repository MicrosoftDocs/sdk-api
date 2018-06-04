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

# D3D11_RLDO_FLAGS enumeration


## -description


Options for the amount of information to report about a device object's lifetime.


## -enum-fields




### -field D3D11_RLDO_SUMMARY


            Specifies to obtain a summary about a device object's lifetime.
          


### -field D3D11_RLDO_DETAIL


            Specifies to obtain detailed information about a device object's lifetime.
          


### -field D3D11_RLDO_IGNORE_INTERNAL


            Do not use this enumeration constant.  
            It is for internal use only.
          


## -remarks




          This enumeration is used by <a href="https://msdn.microsoft.com/a4e5f3c1-8b67-488b-8476-464c5ea5abc6">ID3D11Debug::ReportLiveDeviceObjects</a>.
        


          Several inline functions exist to combine the options using operators, see the D3D11SDKLayers.h header file for details.
        




## -see-also




<a href="https://msdn.microsoft.com/0fd0456b-2638-4b4c-8a34-a3e104a1a034">Core Enumerations</a>
 

 

