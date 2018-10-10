---
UID: NF:winml.IWinMLRuntimeFactory.CreateRuntime
title: IWinMLRuntimeFactory::CreateRuntime
author: windows-sdk-content
description: Creates a WinML runtime.
old-location: machinelearning\iwinmlruntimefactory_createruntime.htm
tech.root: MachineLearning
ms.assetid: 06EE4008-597D-4DA8-A7CD-E70784A2ADC3
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CreateRuntime, CreateRuntime method, CreateRuntime method,IWinMLRuntimeFactory interface, IWinMLRuntimeFactory interface,CreateRuntime method, IWinMLRuntimeFactory.CreateRuntime, IWinMLRuntimeFactory::CreateRuntime, MachineLearning.iwinmlruntimefactory_createruntime, winml/IWinMLRuntimeFactory::CreateRuntime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winml.lib
req.dll: Winml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winml.dll
api_name:
 - IWinMLRuntimeFactory.CreateRuntime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWinMLRuntimeFactory::CreateRuntime


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Creates a WinML runtime.


## -parameters




### -param RuntimeType [in]

A <a href="https://msdn.microsoft.com/5F522511-6186-4C1F-9315-3E382E87F62C">WINML_RUNTIME_TYPE</a> that decribes the type of WinML runtime.


### -param ppRuntime [out]

A pointer to the created <a href="https://msdn.microsoft.com/C2FD74A1-EE38-46B1-98A8-43557485F92E">IWinMLRuntime</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7817A028-031C-49AA-A17A-4364DC0E78D0">IWinMLRuntimeFactory</a>
 

 

