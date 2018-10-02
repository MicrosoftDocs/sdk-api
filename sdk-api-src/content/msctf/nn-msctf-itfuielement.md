---
UID: NN:msctf.ITfUIElement
title: ITfUIElement
author: windows-sdk-content
description: The ITfUIElement interface is a base interface of the UIElement object and is implemented by a text service.
old-location: tsf\itfuielement.htm
tech.root: TSF
ms.assetid: 651c3ca1-5e5b-4978-80d2-2183bd158610
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfUIElement, ITfUIElement interface [Text Services Framework], ITfUIElement interface [Text Services Framework],described, _tsf_itfuielement_ref, msctf/ITfUIElement, tsf.itfuielement
ms.prod: windows
ms.technology: windows-sdk
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
 - ITfUIElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfUIElement interface


## -description


The <a href="https://msdn.microsoft.com/8f77b3bc-2e47-4966-8030-d05a626ee00a">ITfUIElement</a> interface is a base interface of the UIElement object and is implemented by a text service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfUIElement</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfUIElement</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfUIElement</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d6fad13-e90a-4c5a-a735-d6e54f53488f">GetDescription</a>
</td>
<td align="left" width="63%">
Returns the description of the UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0456761e-58fc-4cda-a576-829dd2c1235f">GetGUID</a>
</td>
<td align="left" width="63%">
Get the unique id of this UI element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84253cbe-a30e-4def-b268-0f5f1b7d54dc">IsShown</a>
</td>
<td align="left" width="63%">
Return true if the UI is currently shown by a text service; otherwise false.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/423543d9-f3aa-4a42-89f6-dd1d48967c73">Show</a>
</td>
<td align="left" width="63%">
Shows the text service's UI of this UI element.

</td>
</tr>
</table> 


## -remarks



A text service may implement some other UIElement interface such as <a href="https://msdn.microsoft.com/1f39aa06-3c94-4959-b857-ca61498d5b5c">ITfCandidateListUIElement</a> in the same object that can be obtained by QI. A text service may implement only the <b>ITfUIElement</b> interface to a UI object that does not have to be drawn by the application but the show status can be controlled by the application. A text service that is categorized by GUID_TFCAT_TIPCAP_UIELEMENTENABLED needs to implement ITfUIElement for any UI object.



