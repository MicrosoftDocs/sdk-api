---
UID: NF:manipulations.IManipulationProcessor.put_SupportedManipulations
title: IManipulationProcessor::put_SupportedManipulations
author: windows-sdk-content
description: The SupportedManipulations property is used to indicate which manipulations are supported by an object.
old-location: wintouch\imanipulationprocessor_supportedmanipulations.htm
tech.root: wintouch
ms.assetid: 1909394f-83ec-4e13-81af-3e6c70210865
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],SupportedManipulations property, IManipulationProcessor.SupportedManipulations, IManipulationProcessor.put_SupportedManipulations, IManipulationProcessor::SupportedManipulations, IManipulationProcessor::get_SupportedManipulations, IManipulationProcessor::put_SupportedManipulations, SupportedManipulations property [Windows Touch], SupportedManipulations property [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::SupportedManipulations, manipulations/IManipulationProcessor::get_SupportedManipulations, manipulations/IManipulationProcessor::put_SupportedManipulations, put_SupportedManipulations, wintouch.imanipulationprocessor_supportedmanipulations
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::put_SupportedManipulations


## -description


The <b>SupportedManipulations</b> property is used to indicate which manipulations are supported by an object.

This property is read/write.


## -parameters


## -remarks



With this property you can control which manipulations the supports and which it does not. 
	 For example, you can block all y-translation manipulations while supporting x-translation manipulations.
	 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
        CoInitialize(0);

        hr = spIManipProc.CoCreateInstance(CLSID_ManipulationProcessor, NULL, CLSCTX_ALL);

        MANIPULATION_PROCESSOR_MANIPULATIONS mpm;
        spIManipProc-&gt;get_SupportedManipulations(&amp;mpm);    
        </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/85ddd2d3-cb4b-48ae-8ad4-230be5420abd">MANIPULATION_PROCESSOR_MANIPULATIONS</a>



<a href="https://msdn.microsoft.com/0f8a3e27-a92f-4086-9573-6c7bbe7efd20">Properties</a>
 

 

