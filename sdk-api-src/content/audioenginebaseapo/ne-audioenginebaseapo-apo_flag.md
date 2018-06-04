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

# APO_FLAG enumeration


## -description


The APO_FLAG enumeration defines constants that are used as flags by an audio processing object (APO).

This enumeration is used by the <a href="https://msdn.microsoft.com/library/windows/hardware/dn425140">APO_REG_PROPERTIES</a> structure to help describe the registration properties of an APO.




## -enum-fields




### -field APO_FLAG_NONE

Indicates that there are no flags enabled for this APO.


### -field APO_FLAG_INPLACE

Indicates that this APO can perform in-place processing. This allows the processor to use a common buffer for input and output.


### -field APO_FLAG_SAMPLESPERFRAME_MUST_MATCH

Indicates that the samples per frame for the input and output connections must match.


### -field APO_FLAG_FRAMESPERSECOND_MUST_MATCH

Indicates that the frames per second for the input and output connections must match.


### -field APO_FLAG_BITSPERSAMPLE_MUST_MATCH

Indicates that bits per sample AND bytes per sample container for the  input and output connections must match. 


### -field APO_FLAG_MIXER


### -field APO_FLAG_DEFAULT

The value of this member is determined by the logical OR result of the three preceding members. In other words:

APO_FLAG_DEFAULT = ( APO_FLAG_SAMPLESPERFRAME_MUST_MATCH | APO_FLAG_FRAMESPERSECOND_MUST_MATCH | APO_FLAG_BITSPERSAMPLE_MUST_MATCH ).


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn425140">APO_REG_PROPERTIES</a>
 

 

