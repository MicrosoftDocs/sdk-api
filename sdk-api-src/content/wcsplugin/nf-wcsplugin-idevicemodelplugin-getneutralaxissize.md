---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetNeutralAxisSize
title: IDeviceModelPlugIn::GetNeutralAxisSize
author: windows-sdk-content
description: The IDeviceModelPlugIn::GetNeutralAxisSize function returns the number of data points along the neutral axis that are returned by the GetNeutralAxis function.
old-location: wcs\IDeviceModelPlugIn_GetNeutralAxisSize.htm
tech.root: WCS
ms.assetid: a4b16003-b193-48b8-9dee-9ffb39f9159d
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: GetNeutralAxisSize, GetNeutralAxisSize method [Windows Color System], GetNeutralAxisSize method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetNeutralAxisSize method, IDeviceModelPlugIn.GetNeutralAxisSize, IDeviceModelPlugIn::GetNeutralAxisSize, _color_IDeviceModelPlugIn::GetNeutralAxisSize, wcs.IDeviceModelPlugIn_GetNeutralAxisSize, wcsplugin/IDeviceModelPlugIn::GetNeutralAxisSize
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
 - IDeviceModelPlugIn.GetNeutralAxisSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceModelPlugIn::GetNeutralAxisSize


## -description


The <a href="wcs.IDeviceModelPlugIn::GetNeutralAxisSize">IDeviceModelPlugIn::GetNeutralAxisSize</a> function returns the number of data points along the neutral axis that are returned by the <a href="access.IDeviceModelPlugIn::GetNeutralAxis">GetNeutralAxis</a> function. It is provided so that a Color Management Module (CMM) can allocate an appropriately sized buffer.


## -parameters




### -param pcColors [out]

The number of points that will be returned by a call to <a href="access.IDeviceModelPlugIn::GetNeutralAxis">GetNeutralAxis</a>. Minimum is 2 (black and white).


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

