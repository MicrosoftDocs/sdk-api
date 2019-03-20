---
UID: NE:manipulations.MANIPULATION_PROCESSOR_MANIPULATIONS
title: MANIPULATION_PROCESSOR_MANIPULATIONS (manipulations.h)
author: windows-sdk-content
description: The MANIPULATION_PROCESSOR_MANIPULATIONS enumeration different kinds of manipulation which can be applied on a target object.
old-location: wintouch\manipulation_processor_manipulations.htm
tech.root: wintouch
ms.assetid: 85ddd2d3-cb4b-48ae-8ad4-230be5420abd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MANIPULATION_ALL, MANIPULATION_NONE, MANIPULATION_PROCESSOR_MANIPULATIONS, MANIPULATION_PROCESSOR_MANIPULATIONS enumeration [Windows Touch], MANIPULATION_ROTATE, MANIPULATION_SCALE, MANIPULATION_TRANSLATE_X, MANIPULATION_TRANSLATE_Y, manipulations/MANIPULATION_ALL, manipulations/MANIPULATION_NONE, manipulations/MANIPULATION_PROCESSOR_MANIPULATIONS, manipulations/MANIPULATION_ROTATE, manipulations/MANIPULATION_SCALE, manipulations/MANIPULATION_TRANSLATE_X, manipulations/MANIPULATION_TRANSLATE_Y, wintouch.manipulation_processor_manipulations
ms.topic: enum
req.header: manipulations.h
req.include-header: Manipulations.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - manipulations.h
api_name:
 - MANIPULATION_PROCESSOR_MANIPULATIONS
product: Windows
targetos: Windows
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
req.redist: 
---

# MANIPULATION_PROCESSOR_MANIPULATIONS enumeration


## -description


The <b>MANIPULATION_PROCESSOR_MANIPULATIONS</b> enumeration different kinds of manipulation which can be applied on a target object.


## -enum-fields




### -field MANIPULATION_NONE

Indicates that no manipulations are performed.


### -field MANIPULATION_TRANSLATE_X

Indicates manipulation by moving the target across the horizontal axis.


### -field MANIPULATION_TRANSLATE_Y

Indicates manipulation by moving the target across the vertical axis.


### -field MANIPULATION_SCALE

Indicates manipulation by making the target larger or smaller.


### -field MANIPULATION_ROTATE

Indicates manipulation by rotating the target.


### -field MANIPULATION_ALL

Indicates all manipulations are enabled.


## -remarks



Use this enumeration with the <a href="https://msdn.microsoft.com/1909394f-83ec-4e13-81af-3e6c70210865">SupportedManipulations</a> property to get and 
		  set the kind of manipulation data you want to receive from the <a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a> interface. 
		  You can combine different kinds of manipulations by a bitwise OR.


#### Examples


```cpp

        CoInitialize(0);

        hr = spIManipProc.CoCreateInstance(CLSID_ManipulationProcessor, NULL, CLSCTX_ALL);

        MANIPULATION_PROCESSOR_MANIPULATIONS mpm;
        spIManipProc->get_SupportedManipulations(&mpm);    
        
```





## -see-also




<a href="https://msdn.microsoft.com/a4424d27-c618-4fbe-99f6-70c74d3e2966">Enumerations</a>
 

 

