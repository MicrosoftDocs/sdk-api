---
UID: NF:wcsplugin.IDeviceModelPlugIn.ColorimetricToDeviceColors
title: IDeviceModelPlugIn::ColorimetricToDeviceColors
author: windows-sdk-content
description: Returns the appropriate XYZ colors in response to the specified number of colors, channels, device colors and the proprietary plug-in algorithms.
old-location: wcs\IDeviceModelPlugIn_ColorimetricToDeviceColors.htm
old-project: WCS
ms.assetid: f950b734-f44f-412e-9944-754f88c8620f
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ColorimetricToDeviceColors, ColorimetricToDeviceColors method [Windows Color System], ColorimetricToDeviceColors method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],ColorimetricToDeviceColors method, IDeviceModelPlugIn.ColorimetricToDeviceColors, IDeviceModelPlugIn::ColorimetricToDeviceColors, _color_IDeviceModelPlugIn::ColorimetricToDeviceColors, wcs.IDeviceModelPlugIn_ColorimetricToDeviceColors, wcsplugin/IDeviceModelPlugIn::ColorimetricToDeviceColors
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WcsPlugIn.h
api_name:
-	IDeviceModelPlugIn.ColorimetricToDeviceColors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IDeviceModelPlugIn::ColorimetricToDeviceColors


## -description


Returns the appropriate XYZ colors in response to the specified number of colors, channels, device colors and the proprietary plug-in algorithms.


## -parameters




### -param cColors [in]

The number of colors in the <i>pXYZColors</i> and <i>pDeviceValues</i> arrays.


### -param cChannels [in]

The number of color channels in the <i>pDeviceValues</i> arrays.


### -param pXYZColors [in]

The pointer to the array of incoming XYZColors to convert to device colors.


### -param pDeviceValues [out]

The pointer to an array that contains the resulting outgoing device color values.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -remarks



If <i>cColors</i> or <i>cChannels</i> is zero, the return value is E_FAIL. If there are invalid or out of gamut colors (which may occur if there has been prior processing of the gamut map model), then the return value is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

