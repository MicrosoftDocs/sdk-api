---
UID: NN:msctf.ITfTextInputProcessor
title: ITfTextInputProcessor
author: windows-sdk-content
description: The ITfTextInputProcessor interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service.
old-location: tsf\itftextinputprocessor.htm
tech.root: TSF
ms.assetid: d3fd296b-0009-4fc2-bf91-0ad31454f0e8
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfTextInputProcessor, ITfTextInputProcessor interface [Text Services Framework], ITfTextInputProcessor interface [Text Services Framework],described, _tsf_itftextinputprocessor_ref, msctf/ITfTextInputProcessor, tsf.itftextinputprocessor
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
req.dll: Sptip.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sptip.dll
api_name:
 - ITfTextInputProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfTextInputProcessor interface


## -description


The <b>ITfTextInputProcessor</b> interface is implemented by a text service and used by the TSF manager to activate and deactivate the text service. The manager obtains a pointer to this interface when it creates an instance of the text service for a thread with a call to <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfTextInputProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfTextInputProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfTextInputProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">Activate</a>
</td>
<td align="left" width="63%">
Activates a text service when a user session starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/427190fc-f246-47c6-84e0-a28808a86b6b">Deactivate</a>
</td>
<td align="left" width="63%">
Deactivates a text service when a user session ends.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

