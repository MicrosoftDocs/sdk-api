---
UID: NF:physicalmonitorenumerationapi.GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
title: GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function
author: windows-sdk-content
description: Retrieves the number of physical monitors associated with a Direct3D device.
old-location: monitor\getnumberofphysicalmonitorsfromidirect3ddevice9.htm
tech.root: Monitor
ms.assetid: 1cb0f035-a429-4355-89b8-d8bcd89cb037
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetNumberOfPhysicalMonitorsFromIDirect3DDevice9, GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function [Monitor Configuration], monitor.getnumberofphysicalmonitorsfromidirect3ddevice9, physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
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
 - GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function


## -description


Retrieves the number of physical monitors associated with a Direct3D device.


## -parameters




### -param pDirect3DDevice9 [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a> interface of the Direct3D device.
          


### -param pdwNumberOfPhysicalMonitors [out]

Receives the number of physical monitors associated with the Direct3D device.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

