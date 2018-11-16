---
UID: NN:msctf.ITfTextInputProcessorEx
title: ITfTextInputProcessorEx
author: windows-sdk-content
description: The ITfTextInputProcessorEx interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service.
old-location: tsf\itftextinputprocessorex.htm
tech.root: TSF
ms.assetid: fc762a6f-8d15-4082-9588-fc77fa565549
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITfTextInputProcessorEx, ITfTextInputProcessorEx interface [Text Services Framework], ITfTextInputProcessorEx interface [Text Services Framework],described, _tsf_itftextinputprocessorex_ref, msctf/ITfTextInputProcessorEx, tsf.itftextinputprocessorex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - Msctf.h
api_name:
 - ITfTextInputProcessorEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfTextInputProcessorEx interface


## -description


The <b>ITfTextInputProcessorEx</b> interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service. The manager obtains a pointer to this interface when it creates an instance of the text service for a thread with a call to CoCreateInstance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTextInputProcessorEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfTextInputProcessorEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTextInputProcessorEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b628e803-ea94-4e69-9919-94e4164d5b36">ActivateEx</a>
</td>
<td align="left" width="63%">
Activates a text service when a user session starts. If the text service implements ITfTextInputProcessorEx and ActivateEx is called, ITfTextInputProcessor::Activate will not be called.

</td>
</tr>
</table> 

