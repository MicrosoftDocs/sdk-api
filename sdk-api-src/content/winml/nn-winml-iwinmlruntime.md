---
UID: NN:winml.IWinMLRuntime
title: IWinMLRuntime (winml.h)
description: Represents the runtime to load and evaluate a WinML model.
old-location: machinelearning\iwinmlruntime.htm
tech.root: MachineLearning
ms.assetid: C2FD74A1-EE38-46B1-98A8-43557485F92E
ms.date: 12/05/2018
ms.keywords: IWinMLRuntime, IWinMLRuntime interface, IWinMLRuntime interface,described, MachineLearning.iwinmlruntime, winml/IWinMLRuntime
ms.topic: interface
f1_keywords:
- winml/IWinMLRuntime
dev_langs:
- c++
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
- IWinMLRuntime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinMLRuntime interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Represents the runtime to load and evaluate a WinML model.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWinMLRuntime</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWinMLRuntime</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWinMLRuntime</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlruntime-createevaluationcontext">CreateEvaluationContext</a>
</td>
<td align="left" width="63%">
Creates a WinML evaluation context object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlruntime-evaluatemodel">EvaluateModel</a>
</td>
<td align="left" width="63%">
Evaluates a WinML model.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlruntime-loadmodel">LoadModel</a>
</td>
<td align="left" width="63%">
Loads a WinML model.

</td>
</tr>
</table> 

