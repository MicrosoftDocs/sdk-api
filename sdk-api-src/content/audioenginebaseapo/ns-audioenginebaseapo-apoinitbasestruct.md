---
UID: NS:audioenginebaseapo.APOInitBaseStruct
title: APOInitBaseStruct
author: windows-sdk-content
description: The APOInitBaseStruct structure is the base initialization header that must precede other initialization data in IAudioProcessingObject::Initialize.
old-location: audio\apoinitbasestruct.htm
tech.root: audio
ms.assetid: 15C973AE-B0E8-42FD-9F34-671A6A915B47
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: APOInitBaseStruct, APOInitBaseStruct structure [Audio Devices], PAPOInitBaseStruct, PAPOInitBaseStruct structure pointer [Audio Devices], audio.apoinitbasestruct, audioenginebaseapo/APOInitBaseStruct, audioenginebaseapo/PAPOInitBaseStruct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: audioenginebaseapo.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Audioenginebaseapo.h
api_name:
 - APOInitBaseStruct
product: Windows
targetos: Windows
req.typenames: APOInitBaseStruct
req.redist: 
---

# APOInitBaseStruct structure


## -description


The APOInitBaseStruct structure is the base initialization header that must precede other  
initialization data in <a href="https://msdn.microsoft.com/b73c2e18-ab7b-4e34-9440-f38891f99bf7">IAudioProcessingObject::Initialize</a>. 


## -struct-fields




### -field cbSize

The total size of the structure in bytes.


### -field clsid

The Class ID (CLSID) of the APO.


## -remarks



If the specified CLSID does not match, then the APOInitBaseStruct structure was not designed for this APO, and this is an error condition.  And if the CLSID of the APO changes  
    between versions, then the CLSID may also be used for version management.  In the case where the CLSID is used for version management, a previous version may still be supported by the APO.




## -see-also




<a href="https://msdn.microsoft.com/E33B1F94-4E3A-4EC1-AFB5-FD803FA391BC">APOInitSystemEffects</a>



<a href="https://msdn.microsoft.com/b73c2e18-ab7b-4e34-9440-f38891f99bf7">IAudioProcessingObject::Initialize</a>
 

 

