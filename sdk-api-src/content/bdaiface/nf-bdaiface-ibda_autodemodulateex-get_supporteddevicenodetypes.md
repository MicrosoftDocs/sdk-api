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

# IBDA_AutoDemodulateEx::get_SupportedDeviceNodeTypes


## -description


The <b>get_SupportedDeviceNodeTypes</b> method retrieves a list of the device node types that the demodulator supports.


## -parameters




### -param ulcDeviceNodeTypesMax [in]

Specifies the size of the <i>pguidDeviceNodeTypes</i> array.


### -param pulcDeviceNodeTypes [out]

If <i>pguidDeviceNodeTypes</i> is <b>NULL</b>, receives the number of device node types that the demodulator supports. If <i>pguidDeviceNodeTypes</i> is not <b>NULL</b>, receives the number of node types that were copied into the <i>pguidDeviceNodeTypes</i> array.


### -param pguidDeviceNodeTypes [in, out]

Pointer to an array of GUIDs, or <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If <i>pguidDeviceNodeTypes</i> is <b>NULL</b>, the method returns the number of supported node types in the <i>pulcDeviceNodeTypes</i> parameter. Otherwise, the method copies the node types into the <i>pguidDeviceNodeTypes</i> array, up to a maximum of <i>ulcDeviceNodeTypesMax</i>.




## -see-also




<a href="https://msdn.microsoft.com/ecc642e4-7c36-400c-8a63-639f75b2bbc2">IBDA_AutoDemodulateEx Interface</a>
 

 

