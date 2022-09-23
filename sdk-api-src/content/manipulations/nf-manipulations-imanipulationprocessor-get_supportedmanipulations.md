---
UID: NF:manipulations.IManipulationProcessor.get_SupportedManipulations
title: IManipulationProcessor::get_SupportedManipulations (manipulations.h)
description: The SupportedManipulations property is used to indicate which manipulations are supported by an object. (Get)
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","SupportedManipulations property","IManipulationProcessor.SupportedManipulations","IManipulationProcessor.get_SupportedManipulations","IManipulationProcessor::SupportedManipulations","IManipulationProcessor::get_SupportedManipulations","IManipulationProcessor::put_SupportedManipulations","SupportedManipulations property [Windows Touch]","SupportedManipulations property [Windows Touch]","IManipulationProcessor interface","get_SupportedManipulations","manipulations/IManipulationProcessor::SupportedManipulations","manipulations/IManipulationProcessor::get_SupportedManipulations","manipulations/IManipulationProcessor::put_SupportedManipulations","wintouch.imanipulationprocessor_supportedmanipulations"]
old-location: wintouch\imanipulationprocessor_supportedmanipulations.htm
tech.root: wintouch
ms.assetid: 1909394f-83ec-4e13-81af-3e6c70210865
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],SupportedManipulations property, IManipulationProcessor.SupportedManipulations, IManipulationProcessor.get_SupportedManipulations, IManipulationProcessor::SupportedManipulations, IManipulationProcessor::get_SupportedManipulations, IManipulationProcessor::put_SupportedManipulations, SupportedManipulations property [Windows Touch], SupportedManipulations property [Windows Touch],IManipulationProcessor interface, get_SupportedManipulations, manipulations/IManipulationProcessor::SupportedManipulations, manipulations/IManipulationProcessor::get_SupportedManipulations, manipulations/IManipulationProcessor::put_SupportedManipulations, wintouch.imanipulationprocessor_supportedmanipulations
req.header: manipulations.h
req.include-header: Manipulations_i.c
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IManipulationProcessor::get_SupportedManipulations
 - manipulations/IManipulationProcessor::get_SupportedManipulations
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.SupportedManipulations
 - IManipulationProcessor.get_SupportedManipulations
 - IManipulationProcessor.put_SupportedManipulations
---

# IManipulationProcessor::get_SupportedManipulations


## -description

The <b>SupportedManipulations</b> property is used to indicate which manipulations are supported by an object.

This property is read/write.

## -parameters

## -remarks

With this property you can control which manipulations the supports and which it does not. 
	 For example, you can block all y-translation manipulations while supporting x-translation manipulations.
	 


#### Examples


```cpp

        CoInitialize(0);

        hr = spIManipProc.CoCreateInstance(CLSID_ManipulationProcessor, NULL, CLSCTX_ALL);

        MANIPULATION_PROCESSOR_MANIPULATIONS mpm;
        spIManipProc->get_SupportedManipulations(&mpm);    
        
```

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/api/manipulations/ne-manipulations-manipulation_processor_manipulations">MANIPULATION_PROCESSOR_MANIPULATIONS</a>



<a href="/windows/desktop/wintouch/mtproperties">Properties</a>
