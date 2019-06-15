---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetPrimarySamples
title: IDeviceModelPlugIn::GetPrimarySamples (wcsplugin.h)
author: windows-sdk-content
description: Returns the measurement color for the primary sample.
old-location: wcs\IDeviceModelPlugIn_GetPrimarySamples.htm
tech.root: WCS
ms.assetid: 46253246-e07c-4f55-92fa-91941abaefcd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPrimarySamples, GetPrimarySamples method [Windows Color System], GetPrimarySamples method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetPrimarySamples method, IDeviceModelPlugIn.GetPrimarySamples, IDeviceModelPlugIn::GetPrimarySamples, _color_IDeviceModelPlugIn::GetPrimarySamples, wcs.IDeviceModelPlugIn_GetPrimarySamples, wcsplugin/IDeviceModelPlugIn::GetPrimarySamples
ms.topic: method
req.header: wcsplugin.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IDeviceModelPlugIn.GetPrimarySamples
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeviceModelPlugIn::GetPrimarySamples


## -description


Returns the measurement color for the primary sample.


## -parameters




### -param pPrimaryColor [out]

The primary color type, which is determined by using the hue circle order. If the plugin device model does not natively support primaries for red, yellow, green, cyan, blue, magenta, black and white, it must still return virtual primary data.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions//dd316902(v=vs.85)">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin">IDeviceModelPlugIn</a>
 

 

