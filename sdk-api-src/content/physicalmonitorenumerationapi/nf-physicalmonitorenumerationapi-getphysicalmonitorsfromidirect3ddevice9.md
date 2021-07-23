---
UID: NF:physicalmonitorenumerationapi.GetPhysicalMonitorsFromIDirect3DDevice9
title: GetPhysicalMonitorsFromIDirect3DDevice9 function (physicalmonitorenumerationapi.h)
description: Retrieves the physical monitors associated with a Direct3D device.
helpviewer_keywords: ["GetPhysicalMonitorsFromIDirect3DDevice9","GetPhysicalMonitorsFromIDirect3DDevice9 function [Monitor Configuration]","monitor.getphysicalmonitorsfromidirect3ddevice9","physicalmonitorenumerationapi/GetPhysicalMonitorsFromIDirect3DDevice9"]
old-location: monitor\getphysicalmonitorsfromidirect3ddevice9.htm
tech.root: Monitor
ms.assetid: 1e0e9749-8ee4-42d5-ab7b-182222b6c429
ms.date: 12/05/2018
ms.keywords: GetPhysicalMonitorsFromIDirect3DDevice9, GetPhysicalMonitorsFromIDirect3DDevice9 function [Monitor Configuration], monitor.getphysicalmonitorsfromidirect3ddevice9, physicalmonitorenumerationapi/GetPhysicalMonitorsFromIDirect3DDevice9
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPhysicalMonitorsFromIDirect3DDevice9
 - physicalmonitorenumerationapi/GetPhysicalMonitorsFromIDirect3DDevice9
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - GetPhysicalMonitorsFromIDirect3DDevice9
---

# GetPhysicalMonitorsFromIDirect3DDevice9 function


## -description

Retrieves the physical monitors associated with a Direct3D device.

## -parameters

### -param pDirect3DDevice9 [in]

Pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface of the Direct3D device.

### -param dwPhysicalMonitorArraySize [in]

Number of elements in <i>pPhysicalMonitorArray</i>. To get the required size of the array, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9">GetNumberOfPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param pPhysicalMonitorArray [out]

Pointer to an array of <a href="/windows/win32/api/physicalmonitorenumerationapi/ns-physicalmonitorenumerationapi-physical_monitor">PHYSICAL_MONITOR</a> structures. The caller must allocate the array.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A single Direct3D device can be associated with more than one physical monitor. This function returns a handle and a text description for each physical monitor.
      

When you are done using the monitor handles, close them by passing the <i>pPhysicalMonitorArray</i> array to the <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-destroyphysicalmonitors">DestroyPhysicalMonitors</a> function.

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>