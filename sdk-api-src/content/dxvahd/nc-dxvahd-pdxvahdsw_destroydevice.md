---
UID: NC:dxvahd.PDXVAHDSW_DestroyDevice
title: PDXVAHDSW_DestroyDevice (dxvahd.h)
description: Destroys an instance of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
old-location: mf\pdxvahdsw_destroydevice.htm
tech.root: medfound
ms.assetid: 1d0cc0a4-effb-4dea-b6ba-ca1a4e1e394e
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_DestroyDevice, PDXVAHDSW_DestroyDevice callback, PDXVAHDSW_DestroyDevice callback function [Media Foundation], dxvahd/PDXVAHDSW_DestroyDevice, mf.pdxvahdsw_destroydevice
f1_keywords:
- dxvahd/PDXVAHDSW_DestroyDevice
dev_langs:
- c++
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
- PDXVAHDSW_DestroyDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_DestroyDevice callback function


## -description


Destroys an instance of a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.


## -parameters




### -param hDevice [in]

A handle to the plug-in DXVA-HD device.


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

