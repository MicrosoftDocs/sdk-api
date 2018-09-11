---
UID: NF:wcsplugin.IDeviceModelPlugIn.SetTransformDeviceModelInfo
title: IDeviceModelPlugIn::SetTransformDeviceModelInfo
author: windows-sdk-content
description: Provides the plug-in with parameters to determine where in the transform sequence the specific plug-in occurs.
old-location: wcs\IDeviceModelPlugIn_SetTransformDeviceModelInfo.htm
tech.root: WCS
ms.assetid: 01d0815d-1a6b-48f3-9a81-65df0e185e8f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDeviceModelPlugIn interface [Windows Color System],SetTransformDeviceModelInfo method, IDeviceModelPlugIn.SetTransformDeviceModelInfo, IDeviceModelPlugIn::SetTransformDeviceModelInfo, SetTransformDeviceModelInfo, SetTransformDeviceModelInfo method [Windows Color System], SetTransformDeviceModelInfo method [Windows Color System],IDeviceModelPlugIn interface, _color_IDeviceModelPlugIn::SetTransformDeviceModelInfo, wcs.IDeviceModelPlugIn_SetTransformDeviceModelInfo, wcsplugin/IDeviceModelPlugIn::SetTransformDeviceModelInfo
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
 - IDeviceModelPlugIn.SetTransformDeviceModelInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDeviceModelPlugIn::SetTransformDeviceModelInfo


## -description


Provides the plug-in with parameters to determine where in the transform sequence the specific plug-in occurs.


## -parameters




### -param iModelPosition

TBD


### -param pIDeviceModelOther [in]

A pointer to a <b>IDeviceModelPlugIn</b> interface that contains the other device model in the transform sequence.


#### - uiOtherModelPosition [in]

The one-based model position of the other device model in the workflow of <i>uiNumModels</i>, as provided in the <a href="https://msdn.microsoft.com/ae47dcc5-f771-4586-9086-b4ab1600c1bc">Initialize</a> function.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -remarks



This function is called by the <a href="https://msdn.microsoft.com/8a40215c-6c37-4346-a669-79b7871f265e">CreateMultiProfileTransform</a> function, which is responsible for calling <b>AddRef</b> and <b>Release</b> as appropriate. The function enables plug-in device models to exchange information in a proprietary manner by accessing proprietary plug-in interface functions.

This function will fail if the other device model is a baseline device model, because such models are not plugins and thus inter-plugin communication is not supported.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

