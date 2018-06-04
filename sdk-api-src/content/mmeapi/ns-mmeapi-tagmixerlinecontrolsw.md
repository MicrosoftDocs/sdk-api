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

# tagMIXERLINECONTROLSW structure


## -description



The <b>MIXERLINECONTROLS</b> structure contains information about the controls of an audio line.




## -struct-fields




### -field cbStruct

Size, in bytes, of the <b>MIXERLINECONTROLS</b> structure. This member must be initialized before calling the <a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a> function. The size specified in this member must be large enough to contain the <b>MIXERLINECONTROLS</b> structure. When <b>mixerGetLineControls</b> returns, this member contains the actual size of the information returned. The returned information will not exceed the requested size, nor will it be smaller than the <b>MIXERLINECONTROLS</b> structure.


### -field dwLineID

Line identifier for which controls are being queried. This member is not used if the MIXER_GETLINECONTROLSF_ONEBYID flag is specified for the <a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a> function, but the mixer device still returns this member in this case. The <b>dwControlID</b> and <b>dwControlType</b> members are not used when MIXER_GETLINECONTROLSF_ALL is specified.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.dwControlID

Control identifier of the desired control. This member is used with the MIXER_GETLINECONTROLSF_ONEBYID flag for the <a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a> function to retrieve the control information of the specified control. Note that the <b>dwLineID</b> member of the <b>MIXERLINECONTROLS</b> structure will be returned by the mixer device and is not required as an input parameter. This member overlaps with the <b>dwControlType</b> member and cannot be used in conjunction with the MIXER_GETLINECONTROLSF_ONEBYTYPE query type.


### -field DUMMYUNIONNAME.dwControlType

Class of the desired <a href="https://msdn.microsoft.com/7d109d0e-360f-4a09-8498-15d37d6766b3">Control Types</a>. This member is used with the MIXER_GETLINECONTROLSF_ONEBYTYPE flag for the <a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a> function to retrieve the first control of the specified class on the line specified by the <b>dwLineID</b> member of the <b>MIXERLINECONTROLS</b> structure. This member overlaps with the <b>dwControlID</b> member and cannot be used in conjunction with the MIXER_GETLINECONTROLSF_ONEBYID query type. See dwControlType member description in <a href="https://msdn.microsoft.com/2ddbcf82-9204-43c6-8235-8bce6a55bb36">MIXERCONTROL</a>.


### -field cControls

Number of <a href="https://msdn.microsoft.com/2ddbcf82-9204-43c6-8235-8bce6a55bb36">MIXERCONTROL</a> structure elements to retrieve. This member must be initialized by the application before calling the <a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a> function. This member can be 1 only if MIXER_GETLINECONTROLSF_ONEBYID or MIXER_GETLINECONTROLSF_ONEBYTYPE is specified or the value returned in the <b>cControls</b> member of the <a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a> structure returned for an audio line. This member cannot be zero. If an audio line specifies that it has no controls, <b>mixerGetLineControls</b> should not be called.


### -field cbmxctrl

Size, in bytes, of a single <a href="https://msdn.microsoft.com/2ddbcf82-9204-43c6-8235-8bce6a55bb36">MIXERCONTROL</a> structure. The size specified in this member must be at least large enough to contain the base <b>MIXERCONTROL</b> structure. The total size, in bytes, required for the buffer pointed to by the <b>pamxctrl</b> member is the product of the <b>cbmxctrl</b> and <b>cControls</b> members of the <b>MIXERLINECONTROLS</b> structure.


### -field pamxctrl

Pointer to one or more <a href="https://msdn.microsoft.com/2ddbcf82-9204-43c6-8235-8bce6a55bb36">MIXERCONTROL</a> structures to receive the properties of the requested audio line controls. This member cannot be <b>NULL</b> and must be initialized before calling the <a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a> function. Each element of the array of controls must be at least large enough to contain a base <b>MIXERCONTROL</b> structure. The <b>cbmxctrl</b> member must specify the size, in bytes, of each element in this array. No initialization of the buffer pointed to by this member is required by the application. All members are filled in by the mixer device (including the <b>cbStruct</b> member of each <b>MIXERCONTROL</b> structure) upon returning successfully.


## -see-also




<a href="https://msdn.microsoft.com/82101519-6906-45fd-908f-137e51a56fb8">Audio Mixer Structures</a>



<a href="https://msdn.microsoft.com/7489fcac-fd4c-46cf-8a1a-e4de576974f0">Audio Mixers</a>



<a href="https://msdn.microsoft.com/2ddbcf82-9204-43c6-8235-8bce6a55bb36">MIXERCONTROL</a>



<a href="https://msdn.microsoft.com/a314cdcd-dd52-49f1-92b4-c8e3775dcbe2">MIXERLINE</a>



<a href="https://msdn.microsoft.com/48fa3396-f3ec-411a-9ea7-d7e82d606f14">mixerGetLineControls</a>
 

 

