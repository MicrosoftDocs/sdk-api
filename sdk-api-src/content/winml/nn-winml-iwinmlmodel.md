---
UID: NN:winml.IWinMLModel
title: IWinMLModel (winml.h)
description: Represents a Windows Machine Learning model with corresponding metadata; includes model descriptions (name, author, versioning, etc.), as well as expected inputs and outputs.
helpviewer_keywords: ["IWinMLModel","IWinMLModel interface","IWinMLModel interface","described","MachineLearning.iwinmlmodel","winml/IWinMLModel"]
old-location: machinelearning\iwinmlmodel.htm
tech.root: MachineLearning
ms.assetid: 604ABFCC-9CA0-409D-A3FF-D5C59758462E
ms.date: 12/05/2018
ms.keywords: IWinMLModel, IWinMLModel interface, IWinMLModel interface,described, MachineLearning.iwinmlmodel, winml/IWinMLModel
f1_keywords:
- winml/IWinMLModel
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
- IWinMLModel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinMLModel interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Represents a Windows Machine Learning model with corresponding metadata; includes model descriptions (name, author, versioning, etc.), as well as expected inputs and outputs. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWinMLModel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWinMLModel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWinMLModel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlmodel-enumeratemetadata">EnumerateMetadata</a>
</td>
<td align="left" width="63%">
Gets the metadata of the model.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlmodel-enumeratemodelinputs">EnumerateModelInputs</a>
</td>
<td align="left" width="63%">
Enumerates the WinML model inputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlmodel-enumeratemodeloutputs">EnumerateModelOutputs</a>
</td>
<td align="left" width="63%">
Enumerates the WinML model outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlmodel-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the WinML model description.

</td>
</tr>
</table> 

