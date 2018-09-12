---
UID: NF:physicalmonitorenumerationapi.GetPhysicalMonitorsFromIDirect3DDevice9
title: GetPhysicalMonitorsFromIDirect3DDevice9 function
author: windows-sdk-content
description: Retrieves the physical monitors associated with a Direct3D device.
old-location: monitor\getphysicalmonitorsfromidirect3ddevice9.htm
tech.root: Monitor
ms.assetid: 1e0e9749-8ee4-42d5-ab7b-182222b6c429
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetPhysicalMonitorsFromIDirect3DDevice9, GetPhysicalMonitorsFromIDirect3DDevice9 function [Monitor Configuration], monitor.getphysicalmonitorsfromidirect3ddevice9, physicalmonitorenumerationapi/GetPhysicalMonitorsFromIDirect3DDevice9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: physicalmonitorenumerationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetPhysicalMonitorsFromIDirect3DDevice9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPhysicalMonitorsFromIDirect3DDevice9 function


## -description


Retrieves the physical monitors associated with a Direct3D device.


## -parameters




### -param pDirect3DDevice9 [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a> interface of the Direct3D device.
          


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
 

 

