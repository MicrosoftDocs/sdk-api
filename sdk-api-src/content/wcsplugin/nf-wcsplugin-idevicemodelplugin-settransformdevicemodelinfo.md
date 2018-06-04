---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDeviceModelPlugIn::SetTransformDeviceModelInfo


## -description


Provides the plug-in with parameters to determine where in the transform sequence the specific plug-in occurs.


## -parameters




### -param iModelPosition




### -param pIDeviceModelOther [in]

A pointer to a <b>IDeviceModelPlugIn</b> interface that contains the other device model in the transform sequence.


#### - uiOtherModelPosition [in]

The one-based model position of the other device model in the workflow of <i>uiNumModels</i>, as provided in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> function.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -remarks



This function is called by the <a href="https://msdn.microsoft.com/8a40215c-6c37-4346-a669-79b7871f265e">CreateMultiProfileTransform</a> function, which is responsible for calling <b>AddRef</b> and <b>Release</b> as appropriate. The function enables plug-in device models to exchange information in a proprietary manner by accessing proprietary plug-in interface functions.

This function will fail if the other device model is a baseline device model, because such models are not plugins and thus inter-plugin communication is not supported.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

