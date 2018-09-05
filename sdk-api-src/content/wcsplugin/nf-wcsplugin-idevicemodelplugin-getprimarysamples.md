---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetPrimarySamples
title: IDeviceModelPlugIn::GetPrimarySamples
author: windows-sdk-content
description: Returns the measurement color for the primary sample.
old-location: wcs\IDeviceModelPlugIn_GetPrimarySamples.htm
old-project: WCS
ms.assetid: 46253246-e07c-4f55-92fa-91941abaefcd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetPrimarySamples, GetPrimarySamples method [Windows Color System], GetPrimarySamples method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetPrimarySamples method, IDeviceModelPlugIn.GetPrimarySamples, IDeviceModelPlugIn::GetPrimarySamples, _color_IDeviceModelPlugIn::GetPrimarySamples, wcs.IDeviceModelPlugIn_GetPrimarySamples, wcsplugin/IDeviceModelPlugIn::GetPrimarySamples
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcsplugin.h
req.include-header: 
req.redist: 
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

