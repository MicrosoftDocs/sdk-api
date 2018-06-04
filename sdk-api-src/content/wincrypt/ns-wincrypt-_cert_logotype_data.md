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

# _CERT_LOGOTYPE_DATA structure


## -description


The <b>CERT_LOGOTYPE_DATA</b> structure contains logotype data.


## -struct-fields




### -field cLogotypeImage

The number of elements in the <b>rgLogotypeImage</b> array.


### -field rgLogotypeImage

An array of <a href="https://msdn.microsoft.com/d1dff71c-41e1-4f02-93b4-019d688ed012">CERT_LOGOTYPE_IMAGE</a> structures that contain the logotype images. The <b>cLogotypeImage</b> member contains the number of elements in this array.


### -field cLogotypeAudio

The number of elements in the <b>rgLogotypeAudio</b> array.


### -field rgLogotypeAudio

An array of <a href="https://msdn.microsoft.com/97357faa-2720-4240-a3c3-77abdce8d86d">CERT_LOGOTYPE_AUDIO</a> structures that contain the logotype audio clips. The <b>cLogotypeAudio</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a>
 

 

