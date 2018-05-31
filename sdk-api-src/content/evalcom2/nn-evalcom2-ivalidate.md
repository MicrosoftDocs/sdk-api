---
UID: NN:evalcom2.IValidate
title: IValidate
author: windows-sdk-content
description: The IValidate interface enables authoring tools to validate a Windows Installer package against a set of Internal Consistency Evaluators.
old-location: setup\ivalidate.htm
old-project: Msi
ms.assetid: b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IValidate, IValidate interface, IValidate interface,described, evalcom2/IValidate, setup.ivalidate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: evalcom2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Evalcom2.dll version 3.0.3790.371 or later
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Evalcom2.dll
api_name:
-	IValidate
product: Windows
targetos: Windows
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IValidate interface


## -description


The <b>IValidate</b> interface enables authoring tools to validate a Windows Installer package against a set of <a href="https://msdn.microsoft.com/0789103d-ae34-46be-a9fb-093e066d6d4b">Internal Consistency Evaluators</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValidate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IValidate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IValidate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be0d21ee-bb15-4c6d-9d69-741adf047863">CloseCUB</a>
</td>
<td align="left" width="63%">
Closes the internal consistency evaluator database (.cub file).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7124f467-4efd-4e8b-9ce2-8463779f6fb9">CloseDatabase</a>
</td>
<td align="left" width="63%">
Closes the installation package or merge module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cadf3c6e-6fbb-4d46-b9a8-4f2508f1e8bc">OpenCUB</a>
</td>
<td align="left" width="63%">
Opens an internal consistency evaluator database (.cub file).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f295eea-5f6b-4afa-b0ac-55606086b2b2">OpenDatabase</a>
</td>
<td align="left" width="63%">
Opens an installation package or merge module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e376740e-82fc-44da-b200-c74d73978c6e">SetDisplay</a>
</td>
<td align="left" width="63%">
Registers a callback function to receive ICE display messages (info, warning, and error messages).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/523334f1-4a82-4981-9c77-fffd2b5b561e">SetStatus</a>
</td>
<td align="left" width="63%">
Enables an authoring tool to receive information about the progress of validation through a registered callback function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7a50031-52ac-4ea2-847c-6212706a9cbd">Validate</a>
</td>
<td align="left" width="63%">
Validates the current installation package or merge module against the internal consistency evaluator database.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0">IValidate</a>



<a href="https://msdn.microsoft.com/df38e75e-554c-4a6d-b9ad-8eee5123a16f">Using Evalcom2</a>



<a href="https://msdn.microsoft.com/c96e5682-d43c-460f-8aee-6ba7b0b9769e">Validation Callback Functions</a>
 

 

