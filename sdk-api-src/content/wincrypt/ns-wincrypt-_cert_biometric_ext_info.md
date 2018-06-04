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

# _CERT_BIOMETRIC_EXT_INFO structure


## -description


The <b>CERT_BIOMETRIC_EXT_INFO</b> structure contains a set of biometric information.


## -struct-fields




### -field cBiometricData

The number of elements in the <b>rgBiometricData</b> array.


### -field rgBiometricData

An array of <a href="https://msdn.microsoft.com/544297e2-b6a6-4a33-94b6-47066262506a">CERT_BIOMETRIC_DATA</a> structures that contain the biometric data. The <b>cBiometricData</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>
 

 

