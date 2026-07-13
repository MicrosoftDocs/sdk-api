---
UID: NF:physicalmonitorenumerationapi.GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
title: GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function (physicalmonitorenumerationapi.h)
description: Retrieves the number of physical monitors associated with a Direct3D device.
helpviewer_keywords: ["GetNumberOfPhysicalMonitorsFromIDirect3DDevice9","GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function [Monitor Configuration]","monitor.getnumberofphysicalmonitorsfromidirect3ddevice9","physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromIDirect3DDevice9"]
old-location: monitor\getnumberofphysicalmonitorsfromidirect3ddevice9.htm
tech.root: Monitor
ms.assetid: 1cb0f035-a429-4355-89b8-d8bcd89cb037
ms.date: 12/05/2018
ms.keywords: GetNumberOfPhysicalMonitorsFromIDirect3DDevice9, GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function [Monitor Configuration], monitor.getnumberofphysicalmonitorsfromidirect3ddevice9, physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
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
 - GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
 - physicalmonitorenumerationapi/GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
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
 - GetNumberOfPhysicalMonitorsFromIDirect3DDevice9
---

# GetNumberOfPhysicalMonitorsFromIDirect3DDevice9 function


## -description

Retrieves the number of physical monitors associated with a Direct3D device.

## -parameters

### -param pDirect3DDevice9 [in]

Pointer to the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface of the Direct3D device.

### -param pdwNumberOfPhysicalMonitors [out]

Receives the number of physical monitors associated with the Direct3D device.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>



<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>