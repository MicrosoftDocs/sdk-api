---
UID: NF:wcsplugin.IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack
title: IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack
author: windows-driver-content
description: Returns the appropriate device colors in response to the incoming number of colors, channels, black information, Commission Internationale l'Eclairge XYZ (CIEXYZ) colors and the proprietary plug-in algorithms.
old-location: wcs\IDeviceModelPlugIn_ColorimetricToDeviceColorsWithBlack.htm
old-project: WCS
ms.assetid: 74ec9ace-2468-4b26-a419-781f0b4fd073
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ColorimetricToDeviceColorsWithBlack, ColorimetricToDeviceColorsWithBlack method [Windows Color System], ColorimetricToDeviceColorsWithBlack method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],ColorimetricToDeviceColorsWithBlack method, IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack, IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack, _color_IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack, wcs.IDeviceModelPlugIn_ColorimetricToDeviceColorsWithBlack, wcsplugin/IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WcsPlugIn.h
api_name:
-	IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack


## -description


Returns the appropriate device colors in response to the incoming number of colors, channels, black information, Commission Internationale l'Eclairge XYZ (CIEXYZ) colors and the proprietary plug-in algorithms.


## -parameters




### -param cColors [in]

The number of colors in the <i>pXYZColors</i> and <i>pDeviceValues</i> arrays.


### -param cChannels [in]

The number of color channels in the <i>pDeviceValues</i> arrays.


### -param pXYZColors [out]

A pointer to the array of outgoing <a href="wcs.gamut_map_model_color_structures">XYZColorF structures</a>.


### -param pBlackInformation [in]

A pointer to the <a href="https://msdn.microsoft.com/b90699f6-b42e-4848-947b-76633dc35802">BlackInformation</a>.


### -param pDeviceValues [in]

A pointer to the array of incoming device colors that are to be converted to <a href="wcs.gamut_map_model_color_structures">XYZColorF structures</a>.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL. For extended error information, call <b>GetLastError</b>.




## -remarks



If <i>cColors</i> or <i>cChannels</i> is zero, the return value is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

