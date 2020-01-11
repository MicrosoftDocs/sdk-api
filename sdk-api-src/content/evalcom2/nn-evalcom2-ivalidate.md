---
UID: NN:evalcom2.IValidate
title: IValidate (evalcom2.h)
description: The IValidate interface enables authoring tools to validate a Windows Installer package against a set of Internal Consistency Evaluators.
old-location: setup\ivalidate.htm
tech.root: Msi
ms.assetid: b7c686f8-ed6a-44d6-ab76-f6d6c7d154a0
ms.date: 12/05/2018
ms.keywords: IValidate, IValidate interface, IValidate interface,described, evalcom2/IValidate, setup.ivalidate
f1_keywords:
- evalcom2/IValidate
dev_langs:
- c++
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
req.lib: 
req.dll: Evalcom2.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Evalcom2.dll
api_name:
- IValidate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IValidate interface


## -description


The <b>IValidate</b> interface enables authoring tools to validate a Windows Installer package against a set of <a href="https://docs.microsoft.com/windows/desktop/Msi/internal-consistency-evaluators-ices">Internal Consistency Evaluators</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValidate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IValidate</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub">CloseCUB</a>
</td>
<td align="left" width="63%">
Closes the internal consistency evaluator database (.cub file).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase">CloseDatabase</a>
</td>
<td align="left" width="63%">
Closes the installation package or merge module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub">OpenCUB</a>
</td>
<td align="left" width="63%">
Opens an internal consistency evaluator database (.cub file).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase">OpenDatabase</a>
</td>
<td align="left" width="63%">
Opens an installation package or merge module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay">SetDisplay</a>
</td>
<td align="left" width="63%">
Registers a callback function to receive ICE display messages (info, warning, and error messages).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Enables an authoring tool to receive information about the progress of validation through a registered callback function.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate">Validate</a>
</td>
<td align="left" width="63%">
Validates the current installation package or merge module against the internal consistency evaluator database.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate">IValidate</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/using-evalcom2">Using Evalcom2</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/validation-callback-functions">Validation Callback Functions</a>
 

 

