---
UID: NC:dxvahd.PDXVAHDSW_CreateDevice
title: PDXVAHDSW_CreateDevice (dxvahd.h)
author: windows-sdk-content
description: Creates an instance of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_createdevice.htm
tech.root: medfound
ms.assetid: f76539c8-13a8-4608-87a6-4947f5debb02
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_CreateDevice, PDXVAHDSW_CreateDevice callback, PDXVAHDSW_CreateDevice callback function [Media Foundation], dxvahd/PDXVAHDSW_CreateDevice, mf.pdxvahdsw_createdevice
ms.topic: callback
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_CreateDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDXVAHDSW_CreateDevice callback function


## -description


Creates an instance of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param *pD3DDevice [in]

A pointer to the <b>IDirect3DDevice9Ex</b> interface of the Direct3D device.


### -param *phDevice [out]

Receives a handle to the plug-in DXVA-HD device.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/74c329cc-af54-4cf8-8cb6-eed9e96db4c5">DXVAHDSW_CALLBACKS</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

