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

# GetPhysicalMonitorsFromIDirect3DDevice9 function


## -description



        Retrieves the physical monitors associated with a Direct3D device.


## -parameters




### -param pDirect3DDevice9 [in]


            Pointer to the <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a> interface of the Direct3D device.
          


### -param dwPhysicalMonitorArraySize [in]


            Number of elements in <i>pPhysicalMonitorArray</i>. To get the required size of the array, call <a href="https://msdn.microsoft.com/1cb0f035-a429-4355-89b8-d8bcd89cb037">GetNumberOfPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pPhysicalMonitorArray [out]


            Pointer to an array of <a href="https://msdn.microsoft.com/58eb4999-37d9-472d-aa26-38b19a2287b2">PHYSICAL_MONITOR</a> structures. The caller must allocate the array.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        A single Direct3D device can be associated with more than one physical monitor. This function returns a handle and a text description for each physical monitor.
      


        When you are done using the monitor handles, close them by passing the <i>pPhysicalMonitorArray</i> array to the <a href="https://msdn.microsoft.com/ec9bbadf-93f3-4842-9bcc-e6a76f2f1ccf">DestroyPhysicalMonitors</a> function.
      




## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

