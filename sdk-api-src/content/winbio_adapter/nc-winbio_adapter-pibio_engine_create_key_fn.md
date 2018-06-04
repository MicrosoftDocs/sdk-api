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

# PIBIO_ENGINE_CREATE_KEY_FN callback function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Called by the Windows Biometric Framework to push an HMAC key to the sensor. The returned key identifier will be passed back to the biometric unit when the framework calls <a href="https://msdn.microsoft.com/56BD9A75-2779-4D21-A083-75736DE6880E">EngineAdapterIdentifyFeatureSetSecure</a>. 


## -parameters




### -param Pipeline

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param *Key

Pointer to a buffer that contains the HMAC key.


### -param KeySize

Size, in bytes, of the buffer specified by the <b>Key</b>  parameter.


### -param KeyIdentifier

Pointer to a buffer that receives a key identifier. The format of the buffer is vendor-defined.


### -param KeyIdentifierSize

Size, in bytes, of the buffer specified by the <b>KeyIdentifier</b>  parameter.


### -param ResultSize

Pointer to a variable that receives the size, in bytes, of the data written to the buffer specified by the <b>KeyIdentifier</b>  parameter.


## -returns



If the <b>KeyIdentifier</b> buffer is too small, <b>WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL</b> must be returned, and the required size must be written to <i>ResultSize</i>. The framework will call the API again with a larger buffer.
If the sensor cannot create the key, <b>WINBIO_E_KEY_CREATION_FAILED</b> must be returned.





## -remarks



Only a single key will be in use at any time. If <b>EngineAdapterCreateKey</b> is called when the engine has knowledge of a preexisting key, the preexisting key must be overwritten with the new one.



