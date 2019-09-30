---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetNumChannels
title: IDeviceModelPlugIn::GetNumChannels (wcsplugin.h)
author: windows-sdk-content
description: Returns the number of device channels in the parameter pNumChannels.
old-location: wcs\IDeviceModelPlugIn_GetNumChannels.htm
tech.root: WCS
ms.assetid: 3963eaf1-2516-4ac5-9f9f-9962f9d42adb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNumChannels, GetNumChannels method [Windows Color System], GetNumChannels method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetNumChannels method, IDeviceModelPlugIn.GetNumChannels, IDeviceModelPlugIn::GetNumChannels, _color_IDeviceModelPlugIn::GetNumChannels, wcs.IDeviceModelPlugIn_GetNumChannels, wcsplugin/IDeviceModelPlugIn::GetNumChannels
ms.topic: method
f1_keywords: 
 - "wcsplugin/IDeviceModelPlugIn.GetNumChannels"
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
 - IDeviceModelPlugIn.GetNumChannels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDeviceModelPlugIn::GetNumChannels


## -description


Returns the number of device channels in the parameter <i>pNumChannels</i>.


## -parameters




### -param pNumChannels [out]

A pointer to an unsigned integer representing the number of color channels for your device.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin">IDeviceModelPlugIn</a>
 

 

