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

# DXGI_DEBUG_RLO_FLAGS enumeration


## -description



          Flags used with <a href="https://msdn.microsoft.com/6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA">ReportLiveObjects</a> to specify the amount of info to report about an object's lifetime.
        


## -enum-fields




### -field DXGI_DEBUG_RLO_SUMMARY


            A flag that specifies to obtain a summary about an object's lifetime.
          


### -field DXGI_DEBUG_RLO_DETAIL


            A flag that specifies to obtain detailed info about an object's lifetime.
          


### -field DXGI_DEBUG_RLO_IGNORE_INTERNAL


            This flag indicates to ignore objects which have no external refcounts keeping them alive.
            D3D objects are printed using an external refcount and an internal refcount. 
            Typically, all objects are printed. 
            This flag means ignore the objects whose external refcount is 0, because the application is not responsible for keeping them alive.
          


### -field DXGI_DEBUG_RLO_ALL


            A flag that specifies to obtain both a summary and detailed info about an object's lifetime.
          


## -remarks




          Use this enumeration with <a href="https://msdn.microsoft.com/6CA5C335-08E3-4CC6-A9C9-D7BC6B11C0EA">IDXGIDebug::ReportLiveObjects</a>.
        

<div class="alert"><b>Note</b>  
        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

