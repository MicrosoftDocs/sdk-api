---
UID: NF:winml.IWinMLRuntime.LoadModel
title: IWinMLRuntime::LoadModel
author: windows-sdk-content
description: Loads a WinML model.
old-location: machinelearning\iwinmlruntime_loadmodel.htm
tech.root: MachineLearning
ms.assetid: 75FC42E6-CFFA-4E85-A2D5-80322630E958
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWinMLRuntime interface,LoadModel method, IWinMLRuntime.LoadModel, IWinMLRuntime::LoadModel, LoadModel, LoadModel method, LoadModel method,IWinMLRuntime interface, MachineLearning.iwinmlruntime_loadmodel, winml/IWinMLRuntime::LoadModel
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
 - IWinMLRuntime.LoadModel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWinMLRuntime::LoadModel


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Loads a WinML model.


## -parameters




### -param Path [in]

Path name for the model.


### -param ppModel [out]

A double pointer to an <a href="https://msdn.microsoft.com/604ABFCC-9CA0-409D-A3FF-D5C59758462E">IWinMLModel</a> describing a WinML model.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C2FD74A1-EE38-46B1-98A8-43557485F92E">IWinMLRuntime</a>
 

 

