---
UID: NN:msctf.ITfCandidateListUIElementBehavior
title: ITfCandidateListUIElementBehavior
author: windows-sdk-content
description: This interface is implemented by a text service that has a candidate list UI and its UI can be controlled by the application. The application QI this interface from ITfUIElement and controls the candidate list behavior.
old-location: tsf\itfcandidatelistuielementbehavior.htm
tech.root: TSF
ms.assetid: 3e1c53c6-f356-4b60-bb85-0f5a7251219d
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfCandidateListUIElementBehavior, ITfCandidateListUIElementBehavior interface [Text Services Framework], ITfCandidateListUIElementBehavior interface [Text Services Framework],described, _tsf_itfcandidatelistuielementbehavior_ref, msctf/ITfCandidateListUIElementBehavior, tsf.itfcandidatelistuielementbehavior
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITfCandidateListUIElementBehavior
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCandidateListUIElementBehavior interface


## -description


This interface is implemented by a text service that has a candidate list UI and its UI can be controlled by the application. The application QI this interface from <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> and controls the candidate list behavior.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCandidateListUIElementBehavior</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCandidateListUIElementBehavior</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCandidateListUIElementBehavior</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e9d231c-fd80-45fa-bfd0-6a9e057dccf2">Abort</a>
</td>
<td align="left" width="63%">
Close the candidate list. There is no guarantee that the current selection will be finalized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3602c094-4e8c-456b-9b6d-b0fc10110cff">Finalize</a>
</td>
<td align="left" width="63%">
Finalize the current selection and close the candidate list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3afdfc9-c3e7-4735-b13f-84c45230128a">SetSelection</a>
</td>
<td align="left" width="63%">
Set the selection of the candidate list.

</td>
</tr>
</table> 

