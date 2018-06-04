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

# IDirectDraw7::GetDeviceIdentifier


## -description


Obtains information about the device driver. This method can be used, with caution, to recognize specific hardware installations to implement workarounds for poor driver or chipset behavior.



## -parameters




### -param






#### - dwFlags [in]

This value consists of flags that specify options. The following flag is the only defined flag:



#### DDGDI_GETHOSTIDENTIFIER

Causes <b>GetDeviceIdentifier</b> to return information about the host (typically 2-D) adapter in a system equipped with a stacked secondary 3-D adapter. Such an adapter appears to the application as if it were part of the host adapter, but is typically located on a separate card. When the <i>dwFlags</i> parameter is 0, information on the stacked secondary is returned because this most accurately reflects the qualities of the DirectDraw object involved.


#### - lpdddi [out]

A pointer to a <a href="https://msdn.microsoft.com/3fdec953-72d4-48f8-b540-e2e6ca770b3c">DDDEVICEIDENTIFIER2</a> structure that receives information about the driver.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return DDERR_INVALIDPARAMS.




## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetDeviceIdentifier</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

