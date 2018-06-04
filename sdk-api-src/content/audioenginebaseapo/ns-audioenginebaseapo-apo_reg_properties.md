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

# APO_REG_PROPERTIES structure


## -description


The APO_REG_PROPERTIES structure is used by <a href="https://msdn.microsoft.com/A0D0BAA9-7942-4952-AC9D-087EE7FE6DD0">IAudioProcessingObject::GetRegistrationProperties</a> for returning the registration properties of  an audio processing object (APO).


## -struct-fields




### -field clsid

The class ID for this APO.


### -field Flags

The flags for this APO. This parameter is an enumerated constant of type <a href="https://msdn.microsoft.com/library/windows/hardware/dn425139">APO_FLAG</a>.


### -field szFriendlyName

The friendly name of this APO. This is a string of characters with a max length of 256.


### -field szCopyrightInfo

The copyright info for this APO. This is a string of characters with a max length of 256.


### -field u32MajorVersion

The major version number for this APO.


### -field u32MinorVersion

The minor version number for this APO.


### -field u32MinInputConnections

The minimum number of input connections for this APO.


### -field u32MaxInputConnections

The maximum number of input connections for this APO.


### -field u32MinOutputConnections

The minimum number of output connections for this APO.


### -field u32MaxOutputConnections

The maximum number of output connections for this APO.


### -field u32MaxInstances

The maximum number of instances of this APO.


### -field u32NumAPOInterfaces

The number of interfaces for this APO. 


### -field iidAPOInterfaceList

 




## -see-also




<a href="https://msdn.microsoft.com/A0D0BAA9-7942-4952-AC9D-087EE7FE6DD0">IAudioProcessingObject::GetRegistrationProperties</a>
 

 

