---
UID: NN:winml.IWinMLModel
title: IWinMLModel
author: windows-sdk-content
description: Represents a Windows Machine Learning model with corresponding metadata; includes model descriptions (name, author, versioning, etc.), as well as expected inputs and outputs.
old-location: machinelearning\iwinmlmodel.htm
old-project: MachineLearning
ms.assetid: 604ABFCC-9CA0-409D-A3FF-D5C59758462E
ms.author: windowssdkdev
ms.date: 03/08/2018
ms.keywords: IWinMLModel, IWinMLModel interface, IWinMLModel interface,described, MachineLearning.iwinmlmodel, winml/IWinMLModel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: WINML_TENSOR_DATA_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winml.dll
api_name:
 - IWinMLModel
product: Windows
targetos: Windows
req.lib: Winml.lib
req.dll: Winml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWinMLModel interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Represents a Windows Machine Learning model with corresponding metadata; includes model descriptions (name, author, versioning, etc.), as well as expected inputs and outputs. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWinMLModel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWinMLModel</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ABB51498-44CE-4B98-89FB-ED8B9B8159ED">EnumerateMetadata</a>
</td>
<td align="left" width="63%">
Gets the metadata of the model.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A87B24B0-9463-4022-9054-08F3D7BA5034">EnumerateModelInputs</a>
</td>
<td align="left" width="63%">
Enumerates the WinML model inputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F946AF8E-67BE-4F4B-9BE3-2142CE646B0B">EnumerateModelOutputs</a>
</td>
<td align="left" width="63%">
Enumerates the WinML model outputs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the WinML model description.

</td>
</tr>
</table> 

