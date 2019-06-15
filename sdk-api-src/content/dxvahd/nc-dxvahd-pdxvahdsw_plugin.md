---
UID: NC:dxvahd.PDXVAHDSW_Plugin
title: PDXVAHDSW_Plugin (dxvahd.h)
author: windows-sdk-content
description: Pointer to a function that initializes a software plug-in device for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\pdxvahdsw_plugin.htm
tech.root: medfound
ms.assetid: 1290daa0-a2dd-4067-b74d-e1b3e3edb321
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_Plugin, PDXVAHDSW_Plugin callback, PDXVAHDSW_Plugin callback function [Media Foundation], dxvahd/PDXVAHDSW_Plugin, mf.pdxvahdsw_plugin
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
 - PDXVAHDSW_Plugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDXVAHDSW_Plugin callback function


## -description


Pointer to a function that initializes a software plug-in device for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -parameters




### -param Size [in]

The size of the structure pointed to by the <i>pCallbacks</i> parameter, in bytes.


### -param *pCallbacks [out]

A pointer to an uninitialized <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a> structure. The function fills this structure with pointers to the plug-in device's callback functions. 


## -returns



If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/ns-dxvahd-_dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a> structure contains pointers to callback functions. The software plug-in device must implement these callback functions. The  DXVA-HD device calls the <b>PDXVAHDSW_Plugin</b> function to get the callback function pointers from the plug-in device.


#### Examples


```cpp
HRESULT CALLBACK DXVAHDSW_Plugin(UINT Size, void* pv)
{
    if (Size < sizeof(DXVAHDSW_CALLBACKS))
    {
        return E_INVALIDARG;
    }

    DXVAHDSW_CALLBACKS* pCallbacks = (DXVAHDSW_CALLBACKS*) pv;

    // TODO: Fill in pCallbacks structure.

    return S_OK;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-dxvahd_createdevice">DXVAHD_CreateDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

