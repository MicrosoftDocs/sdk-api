---
UID: NF:d3d11sdklayers.ID3D11Debug.ReportLiveDeviceObjects
title: ID3D11Debug::ReportLiveDeviceObjects method
author: windows-driver-content
description: Report information about a device object's lifetime.
old-location: direct3d11\id3d11debug_reportlivedeviceobjects.htm
old-project: direct3d11
ms.assetid: a4e5f3c1-8b67-488b-8476-464c5ea5abc6
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 734af011-a2b7-a89f-361d-01350006a197, ID3D11Debug, ID3D11Debug interface [Direct3D 11], ReportLiveDeviceObjects method, ID3D11Debug::ReportLiveDeviceObjects, ReportLiveDeviceObjects method [Direct3D 11], ReportLiveDeviceObjects method [Direct3D 11], ID3D11Debug interface, ReportLiveDeviceObjects,ID3D11Debug.ReportLiveDeviceObjects, d3d11sdklayers/ID3D11Debug::ReportLiveDeviceObjects, direct3d11.id3d11debug_reportlivedeviceobjects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Debug.ReportLiveDeviceObjects
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Debug::ReportLiveDeviceObjects method


## -description


Report information about a device object's lifetime.


## -parameters




### -param Flags

Type: <b><a href="https://msdn.microsoft.com/9ab8c5c7-bb4e-4d6b-90fc-5e4cdfba0c71">D3D11_RLDO_FLAGS</a></b>

A value from the
            <a href="https://msdn.microsoft.com/9ab8c5c7-bb4e-4d6b-90fc-5e4cdfba0c71">D3D11_RLDO_FLAGS</a> enumeration.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<b>ReportLiveDeviceObjects</b> uses the value in  <i>Flags</i> to determine the amount of information to report about a device object's lifetime.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug Interface</a>
 

 

