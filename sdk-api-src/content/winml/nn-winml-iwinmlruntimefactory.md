---
UID: NN:winml.IWinMLRuntimeFactory
title: IWinMLRuntimeFactory (winml.h)
author: windows-sdk-content
description: Represents the factory that creates the WinML runtime for model loading and evaluation.
old-location: machinelearning\iwinmlruntimefactory.htm
tech.root: MachineLearning
ms.assetid: 7817A028-031C-49AA-A17A-4364DC0E78D0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWinMLRuntimeFactory, IWinMLRuntimeFactory interface, IWinMLRuntimeFactory interface,described, MachineLearning.iwinmlruntimefactory, winml/IWinMLRuntimeFactory
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
 - IWinMLRuntimeFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinMLRuntimeFactory interface


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

<b>These APIs have been deprecated and should no longer be used:  </b>Please use <a href="https://docs.microsoft.com/uwp/api/windows.ai.machinelearning">Windows.AI.MachineLearning</a> instead.

Represents the factory that creates the WinML runtime for model loading and evaluation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWinMLRuntimeFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWinMLRuntimeFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWinMLRuntimeFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winml/nf-winml-iwinmlruntimefactory-createruntime">CreateRuntime</a>
</td>
<td align="left" width="63%">
Creates a WinML runtime.

</td>
</tr>
</table> 

