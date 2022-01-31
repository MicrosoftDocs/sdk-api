---
UID: NE:manipulations.MANIPULATION_PROCESSOR_MANIPULATIONS
title: MANIPULATION_PROCESSOR_MANIPULATIONS (manipulations.h)
description: The MANIPULATION_PROCESSOR_MANIPULATIONS enumeration different kinds of manipulation which can be applied on a target object.
helpviewer_keywords: ["MANIPULATION_ALL","MANIPULATION_NONE","MANIPULATION_PROCESSOR_MANIPULATIONS","MANIPULATION_PROCESSOR_MANIPULATIONS enumeration [Windows Touch]","MANIPULATION_ROTATE","MANIPULATION_SCALE","MANIPULATION_TRANSLATE_X","MANIPULATION_TRANSLATE_Y","manipulations/MANIPULATION_ALL","manipulations/MANIPULATION_NONE","manipulations/MANIPULATION_PROCESSOR_MANIPULATIONS","manipulations/MANIPULATION_ROTATE","manipulations/MANIPULATION_SCALE","manipulations/MANIPULATION_TRANSLATE_X","manipulations/MANIPULATION_TRANSLATE_Y","wintouch.manipulation_processor_manipulations"]
old-location: wintouch\manipulation_processor_manipulations.htm
tech.root: wintouch
ms.assetid: 85ddd2d3-cb4b-48ae-8ad4-230be5420abd
ms.date: 12/05/2018
ms.keywords: MANIPULATION_ALL, MANIPULATION_NONE, MANIPULATION_PROCESSOR_MANIPULATIONS, MANIPULATION_PROCESSOR_MANIPULATIONS enumeration [Windows Touch], MANIPULATION_ROTATE, MANIPULATION_SCALE, MANIPULATION_TRANSLATE_X, MANIPULATION_TRANSLATE_Y, manipulations/MANIPULATION_ALL, manipulations/MANIPULATION_NONE, manipulations/MANIPULATION_PROCESSOR_MANIPULATIONS, manipulations/MANIPULATION_ROTATE, manipulations/MANIPULATION_SCALE, manipulations/MANIPULATION_TRANSLATE_X, manipulations/MANIPULATION_TRANSLATE_Y, wintouch.manipulation_processor_manipulations
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
targetos: Windows
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MANIPULATION_PROCESSOR_MANIPULATIONS
 - manipulations/MANIPULATION_PROCESSOR_MANIPULATIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - manipulations.h
api_name:
 - MANIPULATION_PROCESSOR_MANIPULATIONS
---

# MANIPULATION_PROCESSOR_MANIPULATIONS enumeration


## -description

The <b>MANIPULATION_PROCESSOR_MANIPULATIONS</b> enumeration different kinds of manipulation which can be applied on a target object.

## -enum-fields

### -field MANIPULATION_NONE:0

Indicates that no manipulations are performed.

### -field MANIPULATION_TRANSLATE_X:0x1

Indicates manipulation by moving the target across the horizontal axis.

### -field MANIPULATION_TRANSLATE_Y:0x2

Indicates manipulation by moving the target across the vertical axis.

### -field MANIPULATION_SCALE:0x4

Indicates manipulation by making the target larger or smaller.

### -field MANIPULATION_ROTATE:0x8

Indicates manipulation by rotating the target.

### -field MANIPULATION_ALL:0xf

Indicates all manipulations are enabled.

## -remarks

Use this enumeration with the <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_supportedmanipulations">SupportedManipulations</a> property to get and 
		  set the kind of manipulation data you want to receive from the <a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a> interface. 
		  You can combine different kinds of manipulations by a bitwise OR.


#### Examples


```cpp

        CoInitialize(0);

        hr = spIManipProc.CoCreateInstance(CLSID_ManipulationProcessor, NULL, CLSCTX_ALL);

        MANIPULATION_PROCESSOR_MANIPULATIONS mpm;
        spIManipProc->get_SupportedManipulations(&mpm);    
        
```

## -see-also

<a href="/windows/desktop/wintouch/rts-functions">Enumerations</a>
