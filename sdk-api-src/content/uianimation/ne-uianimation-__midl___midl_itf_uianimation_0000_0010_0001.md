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

# __MIDL___MIDL_itf_UIAnimation_0000_0010_0001 enumeration


## -description


Defines which aspects of an interpolator  depend on a given input.


## -enum-fields




### -field UI_ANIMATION_DEPENDENCY_NONE

No aspect depends on the input.


### -field UI_ANIMATION_DEPENDENCY_INTERMEDIATE_VALUES

The intermediate values depend on the input.


### -field UI_ANIMATION_DEPENDENCY_FINAL_VALUE

The final value depends on the input.


### -field UI_ANIMATION_DEPENDENCY_FINAL_VELOCITY

The final velocity depends on the input.


### -field UI_ANIMATION_DEPENDENCY_DURATION

The duration depends on the input.


## -remarks



Multiple <b>UI_ANIMATION_DEPENDENCIES</b> values can be combined using a bitwise-OR operation.




## -see-also




<a href="https://msdn.microsoft.com/a897caa9-8a03-465e-8b74-b4614efce00c">IUIAnimationInterpolator::GetDependencies</a>
 

 

